<template>
  <div class="container">
    <header class="jumbotron">
      <h3 style="text-align:center">{{ content }}</h3>
      
    </header>
  </div>
</template>

<script>
// import UserService from "../services/user.service";

export default {
  name: "Home",
  data() {
    return {
      content: "B2E 個網銀後台管理系統",
    };
  },
  // mounted() {
  //   UserService.getPublicContent().then(
  //     (response) => {
  //       this.content = response.data;
  //     },
  //     (error) => {
  //       this.content =
  //         (error.response &&
  //           error.response.data &&
  //           error.response.data.message) ||
  //         error.message ||
  //         error.toString();
  //     }
  //   );
  // },
};
</script>

<style scoped>
.container {
  
}

.jumbotron {
    text-align: center;
  }
</style>