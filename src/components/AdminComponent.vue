<template>
<v-app id="inspire">

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Administración</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
      icon
      class="mr-5"
      @click="salir()">
         <v-icon>mdi-logout</v-icon>
         <span>Salir</span>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      fixed
      temporary
    >
      <v-card
        class="mx-auto"
        width="300"
      >
        <v-list>
          <v-list-item
          :to="{name: 'Home'}">
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>

            <v-list-item-title>Inicio</v-list-item-title>
          </v-list-item>

          <v-list-group
            prepend-icon="mdi-format-list-checks"
          >
              <template v-slot:activator>
                <v-list-item-content>
                  <v-list-item-title>Admin</v-list-item-title>
                </v-list-item-content>
              </template>

              <v-list-item
                v-for="([title, ruta], index) in admins"
                :key="index"
                :to="{name: ruta}"
              >
                <v-list-item-title v-text="title"></v-list-item-title>

                <v-list-item-icon>
                  <v-icon v-text="icon"></v-icon>
                </v-list-item-icon>
              </v-list-item>
            </v-list-group>
<!-- v-if="this.$store.state.user.rol === 'Administrador'" -->
            <v-list-group 
              prepend-icon="mdi-account-edit-outline"
              no-action
            >
              <template v-slot:activator>
                <v-list-item-content>
                  <v-list-item-title>Permisos</v-list-item-title>
                </v-list-item-content>
              </template>
              

              <v-list-item
                v-for="([title, ruta], i) in cruds"
                :key="i"
                link
                :to="{name: ruta}"
              >
                <v-list-item-title v-text="title"></v-list-item-title>

                <v-list-item-icon>
                  <v-icon v-text="icon"></v-icon>
                </v-list-item-icon>
              </v-list-item>
            </v-list-group>
          
        </v-list>
      </v-card>
    </v-navigation-drawer>

    <v-main class="grey lighten-2">
      <v-container>
         <router-view></router-view>

      </v-container>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'AdminComponent',

  components: {
      
  },

  data: () => ({
    //
    drawer: null,
    admins: [
        ['Categorías', 'Categoria'],
        ['Artículos', 'Articulo'],
      ],
      cruds: [
        ['Usuarios', 'Usuario'],
    ],
  }),
  created(){
    this.$store.dispactch('autoLogin');
  },
  methods:{
    salir(){
      this.$store.dispactch('salir'); 
    }
  }
};
</script>
