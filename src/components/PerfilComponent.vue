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
      <div class="w-field-content">
        <v-text-field
          class="w-field-a"
          value="John"
          dense
          readonly
          outlined
        ></v-text-field>
        <v-text-field
          class="w-field-b"
          value="Doe"
          dense
          outlined
          readonly
        ></v-text-field>
      </div>
      <div class="w-field-content">
        <v-text-field
          class="w-field-a"
          value="john.doe@email.com"
          dense
          outlined
          readonly
        ></v-text-field>
        <v-text-field
          class="w-field-b"
          value="+55 (99) 92128-0109"
          dense
          outlined
          readonly
        ></v-text-field>
      </div>
      <div class="w-field-content">
        <v-text-field
          class="w-field-a"
          value="767.834.833-98"
          dense
          outlined
          readonly
        ></v-text-field>
         <v-text-field
          class="w-field-b"
          value="12/02/1982"
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
    flex-direction: column;

    .w-field-content {
      display: flex;
      flex-direction: row;

      .w-field-a {
        margin-left: 100px;
        margin-right: 15px;
      }
      .w-field-b {
        margin-left: 15px;
        margin-right: 100px;
      }
    }
  }
}
</style>
