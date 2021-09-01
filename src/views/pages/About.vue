<template>
  <div class="about">
    <div class="about_title">
      <h1>{{  aboutTitle }}</h1>
    </div>
    <!-- input Section -->
    <div class="input_text_pops">
      <input type="text" v-model="text" placeholder="First enter anything">
      <input type="text" v-model="one" placeholder="second enter anything">
    </div>
    <!-- Proper section part -->
    <Props :btn-text="text" :abc="one"/>
    <!-- Input Button Section part -->
    <div class="last_part_button">
      <button>{{ binding }}</button>
      <button>{{ newzaland }}</button>
    </div>
    <!-- Pages content Section Part -->
    <div class="box_part">
      <div class="header">
        <p>{{ Paragarph }}</p>
        <p>
          {{ liveScore }}
        </p>
      </div>
    </div>


    <!-- Practi With Mounts and before Mounts-->
    <div class="mountes">
      <h1>{{ mountes }}</h1>
    </div>

    <!-- Compuntead Section  -->
    <div class="main_computead">
      <h3>Incrise And Decriss</h3>
      <button v-on:click="a++" class="buttonpart">Add to A</button>
      <button v-on:click="b++" class="buttonpart">Add to B</button>
      <p>A - {{ a }}</p>
      <p>A - {{ b }}</p>
      <!--Component Section-->
      <h2>Computed Proparty</h2>
    </div>



    <!-- ApI Weather Box Box-->
    <div class="api_part">
      <h2>Hello</h2>
      <main>
        <div class="search-box">
          <input
              type="text"
              class="search-bar"
              placeholder="search..."
          />
        </div>

        <div class="weather-wrap">
          <div class="location-box">
            <div class="location">Dhaka, Bangladesh</div>
            <div class="date">Monday 1 September</div>
          </div>

          <div class="weather-box">
            <div class="temp">9*c</div>
            <div class="weather">Rain</div>
          </div>
        </div>

      </main>
    </div>




  </div>
</template>
<script>
import Props from "@/views/component/Props";
export default {
  name:"About",
  components: {
    Props
  },
  data(){
    return{
      api_key:'f6a2c317f97367bfe8fa3e5fc517e80d',
      url_base:"https://www.google.com/",
      query:'',
      weather:{},

      a:0,
      b:0,
      mountes:'Live Cicle Hook And Computed Section',
      aboutTitle: 'About Page Title Part',
      one: '',
      text:'',
      liveScore:'Paragraph Section',
      binding:'Header',
      newzaland:'Other Header',
      Paragarph:'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur eum molestias nisi quasi rem tempora tenetur! Ab facere iste nemo soluta voluptatum? A accusantium asperiores atque corporis culpa deserunt dolores esse facilis fuga impedit itaque labore magni molestiae mollitia nemo nisi nostrum nulla omnis optio quae quaerat, rem reprehenderit voluptatibus!'
    }
  },
  // // Life Cycle hooks
  // beforeCreate() {
  //   alert('Hi Their');
  // },
  // created() {
  //   alert('You Can Click Ok Button');
  // },
  // beforeMount() {
  //   alert('Please Click Again');
  // },
  // mounted() {
  //   alert('Wait A Minute');
  // },
  // beforeUpdate() {
  //   alert('beforeUpdate');
  // },
  // updated() {
  //   alert('update')
  // }
  beforeMount() {
      console.warn(this.$el)
  },
  mounted() {
    console.warn(this.$el)
  }

}

</script>
<style>

</style>