<template>
  <div class="w-full flex">
    <div class="m-auto">
      <h1 class="text-4xl text-pink-900 p-5">Hay there , its is single user page</h1>
      <p>User ID:: <strong v-text="$route.params.id"></strong></p>
    </div>
  </div>
</template>

<script>
    export default {
        name: "users",
      validate(data){
         return /^\d+$/.test(data.params.id);
      }
    }
</script>

<style scoped>

</style>
