<template>
  
    <body>
      <div>
          <div>
            <h1 class=" flex justify-between items-center bg-white dark:bg-gray-900 border-b dark:border-gray-900 p-4 text-gray-700 dark:text-gray-500 text-3xl font-bold">
            <a href="/" class=" rounded-full py-2 px-3 uppercase font-bold tracking-wider cursor-pointer">Sri's Kitchen</a>
            <authentication/>
          </h1>
          </div>
            
          <div>
              <div class="flex justify-center text-gray-700 relative space-x-5 shadow-xl">
              
                <span class="rounded-full py-2 px-2 uppercase text-lg font-bold tracking-wider cursor-pointer "> Home</span>
              
                <span class="rounded-full py-2 px-2 uppercase text-lg font-bold tracking-wider cursor-pointer"> Aout</span>
              
                <span class="rounded-full py-2 px-2 uppercase text-lg font-bold tracking-wider cursor-pointer"> Contact</span>
              
              </div>
            <header class="font-bold pb-5 mt-8 border-b border-gray-200 text-xl shadow-lg">
              Today's Special
            </header>
              <div class="mt-2 grid lg:grid-cols-3 p-3">
                <div class=" rounded bg-white border-gray-200 shadow-md overflow-hidden relative ">
                  <img src="../assets/dosa.jpg" alt="dosa" class="h-32 sm:h-48 w-full object-cover p-4"/>
                  <div>
                   <span class="p-4 text-lg tracking-normal font-bold card hover:shadow-lg">Indian Dosa</span>
                
                  </div>
                </div>
                <div class=" rounded bg-white border-gray-200 shadow-md overflow-hidden relative">
                  <img src="../assets/kaju.jpg" alt="kaju" class="h-32 sm:h-48 w-full object-cover p-4"/>
                  <div>
                   <span class="p-4 text-lg tracking-normal font-bold card hover:shadow-lg">Kaju Katli</span>
                
                  </div>
                </div>
                <div class=" rounded bg-white border-gray-200 shadow-md overflow-hidden relative">
                  <img src="../assets/somaso.jpg" alt="samosa" class="h-32 sm:h-48 w-full object-cover p-4"/>
                  <div>
                   <span class="p-4 text-lg tracking-normal font-bold card hover:shadow-lg">Samosa</span>
                
                  </div>
                </div>
              </div>
            </div>
            <div>
              <header class="font-bold pb-5 mt-8 border-b border-gray-200 text-xl shadow-lg">
                 Most Popular
             </header>
              <div class="mt-2 grid lg:grid-cols-3 p-3">
                <div class=" rounded bg-white border-gray-200 shadow-md overflow-hidden relative ">
                  <img src="../assets/vindaloo.jpg" alt="vindaloo" class="h-32 sm:h-48 w-full object-cover p-4"/>
                  <div>
                   <span class="p-4 text-lg tracking-normal font-bold card hover:shadow-lg">Vindaloo</span>
                
                  </div>
                </div>
                <div class=" rounded bg-white border-gray-200 shadow-md overflow-hidden relative">
                  <img src="../assets/steak.jpg" alt="steak" class="h-32 sm:h-48 w-full object-cover p-4"/>
                  <div>
                   <span class="p-4 text-lg tracking-normal font-bold card hover:shadow-lg">Steak</span>
                
                  </div> 
                </div>
                <div class=" rounded bg-white border-gray-200 shadow-md overflow-hidden relative">
                  <img src="../assets/65.jpg" alt="65" class="h-32 sm:h-48 w-full object-cover p-4"/>
                  <div>
                   <span class="p-4 text-lg tracking-normal font-bold card hover:shadow-lg">Chicken 65</span>
                
                  </div>
                </div>
              </div>
            </div>
          </div>
    </body>
  
</template>

<script>
import authentication from "../components/authentication"
export default {
  components: { authentication },

}
</script>

<style>

</style>