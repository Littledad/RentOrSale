<template>
  <div class="first-page">
    <WelcomeMessage :SearchOrUser="0" />

    <Cates />

    <Swipper />
  </div>
</template>

<script>
import WelcomeMessage from "./components/WelcomeMessage";
import Cates from "./components/Cates";
import List from "./components/List";
import Swipper from "./components/Swipper";

export default {
  name: "FirstPage",
  components: {
    WelcomeMessage,
    Cates,
    List,
    Swipper
  }
};
</script>

<style>
.first-page {
  background-color: rgba(240, 240, 240, 1);
}
</style>
