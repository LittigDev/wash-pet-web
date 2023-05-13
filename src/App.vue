<template>
  <div id="app">
    <div>
      <div class="w-header">
        <img src="./assets/logo-wash.png" width="150" height="45" />
      </div>
      <div class="w-conteiner">
        <v-card
          height="500"
          width="256"
          class="mx-auto w-navigation"
        >
          <v-navigation-drawer permanent>
            <v-list
              dense
              nav
            >
            <v-list-item
              v-for="item in items"
              :key="item.title"
              link
            >
              <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
                </v-list-item-icon>
                <v-list-item-content>
                  <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-navigation-drawer>
        </v-card>
        <div class="w-content">
          <router-view/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'App',
    data () {
      return {
        items: [
          { title: 'Pagina Inicial', icon: 'mdi-home' },
          { title: 'Perfil', icon: 'mdi-face-woman' },
          { title: 'Calendário', icon: 'mdi-calendar-multiselect' },
          { title: 'Serviços', icon: 'mdi-dog-service' },
        ],
        right: null,
      }
    },
  }
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.w-header {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100px;
  border: 1px solid #03AF90;
  background-image: url('./assets/background-header.png');
  background-size: cover;
}
.w-conteiner {
  display: flex;
  flex-direction: row;

  .w-navigation {
    background-color: #F2F2F2;
  }
}
.w-content {
  width: 100%;
  display: flex;
  justify-content: center;
}
</style>
