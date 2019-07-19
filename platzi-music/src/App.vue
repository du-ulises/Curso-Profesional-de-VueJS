<template lang="pug">
  #app
    .columns
      .column
      .column.is-three-fifths
        img(src="./assets/logo.png")
        h1 Registro Estación Platzi
        br
        .field
          label.label Nombre
            .control
              input.input(type="text", name='nombre', placeholder="Nombre")
        .field
          label.label Apellidos
            .control
              input.input(type="text", name='apellidos', placeholder="Apellidos")
        .field
          label.label Cargo
            .control
              input.input(type="text", name='cargo', placeholder="Cargo")
        .field.is-grouped.is-grouped-right
          .control
            button.button.is-primary Enviar
      .column
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hello World'
    }
  }
}
</script>

<style lang="scss">
  @import './scss/main.scss';
  #app {
    margin-top: 5%;
    margin-left: 5%;
    max-width: 420px;
  }
  h1 {
    color: #A3ECF3;
    font-size: 20px;
    font-weight: bolder;
    text-align: center
  }
  img {
    margin:10px auto;
		display:block;
  }
  .label{
    color:#FF9300;
    font-size: 11px;
  }
  .input{
    border: none;
    border-bottom: 1px solid #FF9300;
    box-shadow: none !important;
    color:#212121;
  }
</style>
