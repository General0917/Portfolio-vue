<template>
    <div id="nav">
      <ul class="nav justify-content-stert flag">
          <li>
            <div class="mt-2" v-show="isEnglish" v-on:click="toggleLanguage()">
              <div style="width:32px; height:32px; background-image:url(../assets/jp.svg); background-size:100%;"></div>
              <img src="../assets/jp.svg" alt="日本語" class="border"/>
            </div>
          </li>
          <li>
                <div class="mt-2" v-show="!isEnglish" v-on:click="toggleLanguage()">
                  <div style="width:32px; height:32px; background-image:url(../assets/us.svg); background-size:100%;"></div>
                  <img src="../assets/us.svg" alt="英語" class="border"/>                  
                </div>
          </li>
      </ul>
      <ul class="nav justify-content-center">
          <li class="nav-item">
              <router-link to="/" class="nav-link">Home</router-link>
          </li>
          <li class="nav-item">
              <router-link to="/about" class="nav-link">About</router-link>
          </li>
          <li class="nav-item">
              <router-link to="/contact" class="nav-link">Contact</router-link>
          </li>
      </ul>
    </div>
</template>
<script>
import { EventBus } from "../../libs/EventBus.vue";
export default {
  name: 'myheader',
  data: function() {
    return {
      isEnglish: true,
    }
  },
  methods: {
    toggleLanguage: function() {
      if(this.isEnglish) {
        this.isEnglish = false;
        console.log(this.isEnglish);
      }else {
        this.isEnglish = true;
        console.log(this.isEnglish);
      }
      const isEnglish = this.isEnglish;
      EventBus.$emit('is-english', isEnglish)
    }
  }
}
</script>
<style>
.flag {
  margin-top: -2.8rem;
}
</style>
