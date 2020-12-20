<template>
  <div class="loginBlock d-flex justify-content-center align-items-center">
    <div class="container">
      <div class="row p-3">
        <div class="col-12 col-md-12 loginSeccion">


          <form class="mt-3 pb-3">
              <div>
                  <h2 class="text-info text-left ml-3">Inicio de sesión</h2> 
              </div>
            <div class="form-group">
              <input
                v-model="login.email"
                type="email"
                class="form-control"
                id="Email-input"
                aria-describedby="emailHelp"
                placeholder="Ingrese su email"/>
              <small id="emailHelp" class="ml-3 form-text text-info text-left">
                  Nunca compartiremos su correo electrónico con nadie más</small>
            </div>
            <div class="form-group">
              <input
                v-model="login.password"
                type="password"
                class="form-control"
                id="Password-input"
                placeholder="Ingrese su Password"/>

            </div>
            <button
              @click.prevent="loginUser"
              type="submit"
              class="btn btn-info">
              Iniciar sesión
            </button>
          </form>

        </div>
      </div>

    </div>

    
  </div>

  
</template>


<script>
import swal from 'sweetalert';
import axios from "axios";

export default {
  name: "TheLogin",
  data() {
    return {
      login: {
        email: "",
        password: "",
      },
    };
  },
  beforeCreate(){
    this.$store.dispatch('autoLogin')
  },
  methods: {
    loginUser() {
      console.log(`nuestra Respuesta  ${this.email}`)
      axios.post("http://localhost:3000/api/usuario/login", this.login)
      .then(response => {
        return response.data;
      })
      .then(data => {
        this.$store.dispatch("guardarToken", data.tokenReturn)
        this.$router.push({name: 'Admin'});
        swal("Acceso concedido!!", "Se ha logueado correctamente!", "success");
        console.log(data);
      })
      .catch(error =>{
        swal("Algo salió mal!", "Error al intentar iniciar sesión", "error");
        console.log(error);
        return error;
      })
    },
  },
};
</script>

<style scoped>
div.loginBlock {
  background-image: url("../../../public/img/bckgdLogin.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 100%;
  position: absolute;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: center;
  align-items: center;
  align-content: stretch;
}

.container {
  background: #fff;
  border-radius: 10px;
  -webkit-box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.7);
  box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.7);
  border: 3px solid #34a7d0;
  max-width: 900px;
}

.loginSeccion {
  padding: 0 2rem;
  position: relative;
  align-self: center;
}

h2{
    font-size: 20px;
}

.logoLogin {
  width: 70%;
  max-width: 768px;
  height: auto;
}

form div.form-group input#Email-input.form-control {
  border: none;
  border-radius: 0;
  border-bottom: 1px solid #81d4fa;
  background-image: url("../../../public/img/icon-email.svg");
  background-repeat: no-repeat;
  background-size: 1rem;
  background-position: 0.5rem center;
  padding: 0.5rem 2rem;
  background-color: #fff; }

form div.form-group input#Password-input.form-control {
  border: none;
  border-radius: 0;
  border-bottom: 1px solid #81d4fa;
  background-image: url("../../../public/img/icon-pass.svg");
  background-repeat: no-repeat;
  background-size: 1rem;
  background-position: 0.5rem center;
  padding: 0.5rem 2rem; }

/* ---- ---- RESPONSIVE ---- ---- */
@media (max-width: 767px) and (min-width: 300px) {
    .container {
        width: 90%;
    }

    .loginSeccion {
      padding: 0;
      position: relative;
      align-self: center;
    }

    .logoLogin {
      width: 100%;
    }
}

/* iPad portrait */
@media (min-width: 768px) and (orientation: portrait){
    .container {
        width: 70%;
    }
}

/* iPad Landscape */
@media only screen and (min-width: 1024px) and (orientation: landscape) {
    .container {
        width: 50%;
    }
    
    .logoLogin {
        width: 100%;
    }
}
</style>