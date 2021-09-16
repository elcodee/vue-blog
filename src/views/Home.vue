<template>
  <div class="home">
    <Navbar />
    <div>
      <b-img
        src="https://bintoroarchitect.co.id/media/bintoroarchitect-Tips-and-Tricks.webp"
        width="2000"
        height="800"
        style="margin-top: -8em"
      ></b-img>
    </div>
    <div class="container mt-3">

      <div class="row">
        <div class="col">
          <Card />
        </div>
      </div>

    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Card from "@/components/Card.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    Card,
  },
};
</script>
