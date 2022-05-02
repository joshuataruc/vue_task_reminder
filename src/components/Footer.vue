<template>
  <footer>
    <p>Copyright &copy; 2022</p>
    <router-link to="/About" v-show="linkChange">About</router-link>
  </footer>
</template>

<script>
export default {
  name: "FooterComponents",
  computed: {
    linkChange() {
      if (this.$route.path === "/About") {
        return false;
      } else {
        return true;
      }
    },
  },
};
</script>

<style scoped>
a {
  color: #333;
}
footer {
  margin-top: 30px;
  text-align: center;
}
</style>