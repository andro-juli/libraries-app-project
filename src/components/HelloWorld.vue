<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <button type="button" class="btn btn-primary">Primary</button>
    <button type="button" class="btn btn-secondary">Secondary</button>
    <button type="button" class="btn btn-success">Success</button>
    <button type="button" class="btn btn-danger">Danger</button>
    <button type="button" class="btn btn-warning">Warning</button>
    <button type="button" class="btn btn-info">Info</button>
    <button type="button" class="btn btn-light">Light</button>
    <button type="button" class="btn btn-dark">Dark</button>

    <button type="button" class="btn btn-link">Link</button>

    <div class="vueper-slides">
      <vueper-slides>
        <vueper-slide v-for="i in 5" :key="i" :title="i.toString()" />
      </vueper-slides>
    </div>

    <div>
      <carousel>
        <slide>
          <div><img src="../assets/cat.jpg" class="image" alt="" /></div>
        </slide>
        <slide>
          <div><img src="../assets/cat2.png" class="image" alt="" /></div>
        </slide>
        <slide>
          <div>
            <img src="../assets/home_dog.png" class="image" alt="" />
          </div>
        </slide>
      </carousel>
    </div>
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "HelloWorld",
  components: { VueperSlides, VueperSlide, Carousel, Slide },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.vueper-slides {
  background: blue;
  color: white;
}
.image {
  width: 60%;
  height: 250px;
}
</style>
