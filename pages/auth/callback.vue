<template>
  <div classe="p-4">signing you in...</div>
</template>
<script>
export default {
  async mounted() {
    try {
      await this.$auth.fetchUser();
      this.$router.replace("/");
    } catch (err) {
      console.err("login failed:", error);
      this.$router.push("/auth/signin");
    }
  },
};
</script>
