<template>
    <div id="stories" class="container SecCasos pb-5">
        <div>
            <h2 class="text-center font-weight-normal pl-5 ml-5">Casos de éxito</h2>
        </div>
    
        <div class="row justify-content-evenly">
            <div class="mt-5 pt-5 col-sm-12 col-md-4">

                <div class="card bg-light border border-info shadow">
                    <!-- <img :src="member.image" class="card-img-top mx-auto d-block mt-3" alt="Logo cliente" style="border-radius: 50%; width: 50%;"> -->
                    <img src="../../public/img/logoBanpolombia.png" class="card-img-top mx-auto d-block mt-3" alt="Logo cliente" style="width: 50%;">
                    <div class="card-body">
                        <!-- <h4 class="card-title text-light text-center">{{member.nombre}}</h4> -->
                        <h4 class="card-title text-light text-center">BanPolombia</h4>
                        <p class="card-text text-dark text-center"><em>"Dejamos en manos de Quantica Ingeniería toda nuestra campaña de sensibilización para usar la App de nuestro banco, hoy el 90% de nuestros clientes usan nuestra app, tuvimos un incremento en descargas desde las tiendas de iOS y Android de un 45%."</em></p>
                    </div>
                </div>
            </div>

            <div class="mt-5 pt-5 col-sm-12 col-md-4">

                <div class="card bg-light border border-info shadow">
                    <!-- <img :src="member.image" class="card-img-top mx-auto d-block mt-3" alt="Logo cliente" style="border-radius: 50%; width: 50%;"> -->
                    <img src="../../public/img/logoSinpatria.png" class="card-img-top mx-auto d-block mt-3" alt="Logo cliente" style="width: 50%;">
                    <div class="card-body">
                        <!-- <h4 class="card-title text-info text-center">{{member.nombre}}</h4> -->
                        <h4 class="card-title text-light text-center">BanPolombia</h4>
                        <p class="card-text text-dark text-center"><em>"Dejamos en manos de Quantica Ingeniería toda nuestra campaña de sensibilización para usar la App de nuestro banco, hoy el 90% de nuestros clientes usan nuestra app, tuvimos un incremento en descargas desde las tiendas de iOS y Android de un 45%."</em></p>
                    </div>
                </div>
            </div>

            <div class="mt-5 pt-5 col-sm-12 col-md-4">

                <div class="card bg-light border border-info shadow">
                    <!-- <img :src="member.image" class="card-img-top mx-auto d-block mt-3" alt="Logo cliente" style="border-radius: 50%; width: 50%;"> -->
                    <img src="../../public/img/logoEvilCorp.png" class="card-img-top mx-auto d-block mt-3" alt="Logo cliente" style="width: 50%;">
                    <div class="card-body">
                        <!-- <h4 class="card-title text-light text-center">{{member.nombre}}</h4> -->
                        <h4 class="card-title text-light text-center">BanPolombia</h4>
                        <p class="card-text text-dark text-center"><em>"Dejamos en manos de Quantica Ingeniería toda nuestra campaña de sensibilización para usar la App de nuestro banco, hoy el 90% de nuestros clientes usan nuestra app, tuvimos un incremento en descargas desde las tiendas de iOS y Android de un 45%."</em></p>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>
<script>
export default {
    name: 'SecCasosExito'
}
</script>
<style scoped>
#stories{
    padding-top: 80px !important;
}

h2{
    color: #00ACC1;
    text-align: left !important;
}

.card{
    border-radius: 80px 10px 80px 10px;
    padding: 1rem;
}

.card-title{
    background-color: #17a2b8;
    padding: 0.4rem;
    border-radius: 20px;
}


</style>