<template>
 <section class="section">
    <div class="container">
      <div class="columns flex justify-center content-center">
        <div>
          <h2 class="flex content-center text-2xl py-20">Register!</h2>

          <Notification :message="error" v-if="error"/>

          <form method="post" @submit.prevent="register">
            <div class="field">
              <label class="label p-2 font-bold">Username</label>
              <div class="control border-gray-900 border-teal p-2 border-t-12 bg-grey-300 mb-2 rounded-lg shadow-lg ">
                <input
                  type="text"
                  class="input"
                  name="username"
                  v-model="username"
                  required
                >
              </div>
            </div>
            <div class="field">
              <label class="label p-2 font-bold">Email</label>
              <div class="control border-gray-900 border-teal p-2 border-t-12 bg-grey-300 mb-2 rounded-lg shadow-lg ">
                <input
                  type="email"
                  class="input"
                  name="email"
                  v-model="email"
                  required
                >
              </div>
            </div>
            <div class="field">
              <label class="label p-2 font-bold">Password</label>
              <div class="control border-gray-900 border-teal p-2 border-t-12 bg-grey-300 mb-2 rounded-lg shadow-lg ">
                <input
                  type="password"
                  class="input"
                  name="password"
                  v-model="password"
                  required
                >
              </div>
            </div>
            <div class="control p-2 font-bold">
              <button type="submit">Register</button>
            </div>
          </form>

          <div>
            Already got an account? <nuxt-link class="control p-2 font-bold" to="/login">Log In</nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      email: '',
      password: '',
      error: null
    }
  },

  methods: {
    async register() {
      try {
        await this.$axios.post('register', {
          username: this.username,
          email: this.email,
          password: this.password
        })

        await this.$auth.loginWith('local', {
          data: {
            email: this.email,
            password: this.password
          },
        })

        this.$router.push('/')
      } catch (e) {
        this.error = e.response.data.message
      }
    }
  }

}
</script>

<style>

</style>