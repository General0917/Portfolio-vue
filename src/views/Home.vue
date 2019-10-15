<template>
<div class="home">
  <div class="top container bg-light" v-show="!isEnglish">
    Hello World.
  </div>
  <div class="bottom">
    <div class="mt-5 h4">
      Welcome to my portfolio page!
    </div>
    <hr class="mb-5 mt-0 d-inline-block mx-auto" style="width: 27em;">
    <div class="container bg-light">
      <div class="my-3 py-3 px-2 txt border">
        These pages are written in <a href="https://vuejs.org/"><font class="text-success font-weight-bold"><font-awesome-icon :icon="['fab','vuejs']"/>vue.js</font></a>,  <a href="https://bootstrap-vue.js.org/"><font class="font-weight-bold" color="purple"><font-awesome-icon :icon="['fab','bootstrap']"/>bootstrap4</font></a> and <a href="https://github.com/FortAwesome/vue-fontawesome"><font class="text-primary font-weight-bold"><font-awesome-icon :icon="['fab','font-awesome']"/>fontawesome</font></a>.
      </div>
      <div class="my-3 py-3 px-2 txt border">
        When I tackled to create this website, there were some difficulties.<br>
        This is mostly because my understanding of vue.js was lacking.<br>
        Also, I was struggling to install fontawesome to my website.
      </div>
      <div class="my-3 py-3 px-2 txt border">
        I'll attach a link to Qiita that describes the solution I used is written below.
      </div>
    </div>
  </div>
</div>
</template>
<style>
  .home {
    padding-bottom: 6rem;
  }
  .top {
    font-size: 70px;
    padding: 100px 0;
    font-weight: bold;
  }
  .bottom {
    margin-bottom: 25px;
  }
  .txt {
    display: inline-block;
    letter-spacing: .1em;
    text-align: start;
  }
</style>
<script>
import  EventBus  from "../../libs/EventBus";
export default {
  name: 'home',
  data: function(){
    return {
      isEnglish: ''
    }
  },
  methods: {
    updateData (isEnglish) {
      this.isEnglish = isEnglish;
    }
  },
  mounted() {
    EventBus.$on('is-english', (isEnglish) => {
      this.updateData(isEnglish)
    })
  }
}
</script>
