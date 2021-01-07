<template>
  <nav>
            <div class="flex justify-center md:justify-end">
              <div class="px-3 py-4 md:col-span-2">
                <nuxt-link class="rounded-full py-2 px-3 uppercase text-xs font-bold tracking-wider cursor-pointer text-primary border-primary md:border-2 hover:bg-primary hover:text-white transition ease-out duration-500" to="/login">Log In</nuxt-link>
              </div>
              <div class="px-5 py-4 md:col-span-2">
                <nuxt-link class="rounded-full py-2 px-3 uppercase text-xs font-bold tracking-wider cursor-pointer text-primary border-primary md:border-2 hover:bg-primary hover:text-white transition ease-out duration-500" to="/signup">Sign Up</nuxt-link>
              </div>
            </div>
          </nav>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
computed: {
    ...mapGetters(['isAuthenticated', 'loggedInUser'])
  },
  name: "authentication"
}
</script>

<style>

</style>