<template>
  <div class="modal-auth" v-if="show" @click="hideDialog">
    <div @click.stop class="modal-dialog modal-dialog-auth">
      <button class="close-auth" @click="hideDialog">&times;</button>
      <form id="logInForm">
        <fieldset class="modal-body">
          <legend class="modal-title">Авторизация</legend>
          <label class="label-auth">
            <span>Логин</span>
            <input id="login" type="text" required/>
          </label>
          <label class="label-auth">
            <span>Пароль</span>
            <input id="password" type="password" required/>
          </label>
        </fieldset>
        <!-- /.modal-body -->
        <div class="modal-footer">
          <div class="footer-buttons">
            <button class="button button-primary button-login" type="submit">
              Войти
            </button>
          </div>
        </div>
      </form>
      <!-- /.modal-footer -->
    </div>
    <!-- /.modal-dialog -->
  </div>
</template>

<script>
export default {
  name: 'modal-auth',
  props: {
    show: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    hideDialog() {
      this.$emit('update:show', false)
    },
  },
}
</script>

<style></style>
