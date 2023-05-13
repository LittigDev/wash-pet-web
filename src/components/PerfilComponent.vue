<template>
  <div class="w-perfil-content">
    <div class="w-avatar-content">
      <v-avatar
        size="120"
      >
        <img
          src="https://cdn.vuetifyjs.com/images/john.jpg"
          alt="John"
        >
      </v-avatar>
    </div>
    <div class="w-form-content">
      <div>        
        <v-text-field
          value="John Doe"
          dense
          outlined
          readonly
        ></v-text-field>
        <v-text-field
          value="John Doe"
          dense
          outlined
          readonly
        ></v-text-field>
      </div>
      <div>
        <v-text-field
          value="John Doe"
          dense
          outlined
          readonly
        ></v-text-field>
        <v-text-field
          value="John Doe"
          dense
          outlined
          readonly
        ></v-text-field>
      </div>
      <div>
        <v-text-field
          value="John Doe"
          dense
          outlined
          readonly
        ></v-text-field>
        <v-text-field
          value="John Doe"
          dense
          outlined
          readonly
        ></v-text-field>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'PerfilComponent'
  }
</script>

<style lang="scss">
.w-perfil-content {
  width: 100%;
  height: 100%;

  .w-avatar-content {
    margin-top: 50px;
    margin-bottom: 30px;
  }

  .w-form-content {
    display: flex;
    justify-content: center;
  }
}
</style>
