<template>
  <section class="bg ">
    <div class="container">
      <div class="flex justify-center content-center">
        <div class="">
          <h2 class="flex content-center text-2xl py-20">Welcome back!</h2>

          <Notification :message="error" v-if="error"/>

          <form method="post" @submit.prevent="login" class=" border-black">
            <div class="field">
              <label class="label p-2 font-bold">Email</label>
              <div class=" border-gray-900 border-teal p-2 border-t-12 bg-grey-300 mb-2 rounded-lg shadow-lg ">
                <input
                  type="email"
                  class="input"
                  name="email"
                  placeholder="Your Username"
                  v-model="email" 
                >
              </div>
            </div>
            <div class="field">
              <label class="label p-2 font-bold">Password</label>
              <div class="border-teal p-2 border-t-12 bg-grey-300 mb-2 rounded-lg shadow-lg ">
                <input
                  type="password"
                  class="input "
                  name="password"
                  placeholder="Your Password"
                  v-model="password"
                >
              </div>
            </div>
            <div class="rounded-full py-1 px-1 uppercase  
            font-bold tracking-wider cursor-pointer text-primary border-primary md:border-2 hover:bg-primary hover:text-white transition ease-out duration-500">
              <button type="submit" class="p-2 font-bold">Log In</button>
            </div>
          </form>
          <div class="has-text-centered" style="margin-top: 20px">
            <p>
              Don't have an account? <nuxt-link to="/signup">Register</nuxt-link>
            </p>
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
      email: '',
      password: '',
      error: null
    }
  },

  methods: {
    async login() {
      try {
        await this.$auth.loginWith('local', {
          data: {
            email: this.email,
            password: this.password
          }
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