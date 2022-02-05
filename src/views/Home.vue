<template>
  <div class="home">
    <homeBody />
  </div>
</template>

<script>
// @ is an alias to /src
import homeBody from "@/components/Home/homeBody.vue";

export default {
  name: "Home",
  components: {
    homeBody,
  },
};
</script>
