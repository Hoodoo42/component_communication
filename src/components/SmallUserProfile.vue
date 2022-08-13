<template>
  <div>
    <section>
      <h3>{{ user[`name`] }}</h3>
      <h4>{{ user[`age`] }}</h4>
      <h4>Premium Status:{{ user[`is_premium`] }}</h4>
    </section>
  </div>
</template>

<script>
export default {
  // this is the info being requested from app.vue that sup.vue will use to display in its section
  props: {
    user: Object,
  },
};
</script>

<style scoped>
</style>