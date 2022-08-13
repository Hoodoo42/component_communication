<template>
  <div id="app">
    <!-- this is using the component SmallUserProfile and its creating a loop that will display the data from app.vue, and is also-->
    <!-- sending down the prop that SmallUserProfile is expecting so that SUP.vue can take the data and display -->
    <small-user-profile v-for="user in users" :key="user[`id`]" :user="user">
    </small-user-profile>
  </div>
</template>

<script>
import SmallUserProfile from "@/components/SmallUserProfile.vue";

export default {
  data() {
    return {
      users: [
        {
          name: `Lorna`,
          age: 23,
          is_premium: true,
          id: 3698,
        },
        {
          name: `Robin`,
          age: 16,
          is_premium: false,
          id: 1982,
        },
        { name: `Sylvia`, age: 42, is_premium: true, id: 1276 },
      ],
    };
  },

  name: "App",
  components: {
    SmallUserProfile,
  },
};
</script>

<style>
</style>
