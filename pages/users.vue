<template>
  <section>
    <article>
      <h1 class="text-4xl">
        <a href="users" class="text-red-900">User</a><!-- here will send normal request-->
        <nuxt-link to="users" class="text-green-700">User</nuxt-link>
        <input v-model="userId"><button @click="loadUser">Load</button>
      </h1>
    </article>
    <NuxtChild />
  </section>
</template>

<script>
  export default {
    name: "users",
    data() {
      return {
        userId: ""
      }
    },
    methods: {
      loadUser() {
        return this.$router.push(`/users/${this.userId}`);
      }
    },
    layout:'test',
  }
</script>

<style scoped>

</style>
