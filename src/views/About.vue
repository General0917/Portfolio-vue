<template>
  <div id="about" class="about">
    <div class="top container bg-light">
      About Me.
    </div>
    <div class="bottom container">
      <div class="mt-5 h4">
        My name is Shunya Endoh!
      </div>
      <hr class="mb-5 mt-0 d-inline-block mx-auto" style="width: 27em;">
      <div class="skills mb-5 py-3 bg-light">
        <div class="skills-title h3 pt-3" v-on:click="isShowDoughnat ? showBarChart() : showDoughnatChart()">skills</div>
        <div class="row doughnat-chart" v-show="isShowDoughnat">
          <div class="col-lg-3 col-12 my-3" v-on:click="toggleHTML()">
            <div v-show="isShowHTML">
              <doughnut :chartdata="{datasets: [{backgroundColor:['coral','gray'], data: [75, 25]}]}" class="doughnat"/>
              <div>HTML</div>
            </div>
            <div class="txt mt-2 py-3 px-3 border" v-show="!isShowHTML">
              <p class="h4">
                <font-awesome-icon :icon="['fab','html5']" class="text-dark"/>     
                HTML
              </p>              
              At a first glance, I can understand construction almost.</div>
          </div>
          <div class="col-lg-3 com-12 my-3" v-on:click="toggleCSS()">
            <div v-show="isShowCSS">
              <doughnut :chartdata="{datasets: [{backgroundColor:['deeppink','gray'], data: [45, 55]}]}" class="doughnat"/>
              <div>CSS</div>
            </div>
            <div class="txt mt-2 py-3 px-3 border" v-show="!isShowCSS">
              <p class="h4">
                <font-awesome-icon :icon="['fab','css3-alt']" class="text-dark"/>     
                CSS
              </p>              
              I'm going to study about "CSS design". Something like BEM.</div>
          </div>
          <div class="col-lg-3 col-12 my-3" v-on:click="toggleJs()">
            <div v-show="isShowJs">
              <doughnut :chartdata="{datasets: [{backgroundColor:['darkseagreen','gray'], data: [55, 45]}]}" class="doughnat"/>
              <div>Javascript</div>
            </div>
            <div class="txt mt-2 py-2 px-3 border" v-show="!isShowJs">
              <p class="h4">
                <font-awesome-icon :icon="['fab','js-square']" class="text-dark"/>                     
                Javascript
                </p>
              I'm intersted in vue.js, React. I have experienced using some libraries. (Actually, I used Chart.js for creating this chart!)</div>
          </div>
          <div class="col-lg-3 col-12 my-3" v-on:click="togglePHP()">
            <div v-show="isShowPHP">
              <doughnut :chartdata="{datasets: [{backgroundColor:['#007BFF','gray'], data: [65, 35]}]}" class="doughnat"/>
              <div>PHP</div>
            </div>
            <div class="txt mt-2 py-2 px-3 border" v-show="!isShowPHP">
              <p class="h4">
                <font-awesome-icon :icon="['fab','php']" class="text-dark"/>                     
                PHP
              </p>
              I have made some web apps with PHP. I can use Laravel framework.
              </div>
          </div>
        </div>

          <div class="bar-chart my-5" v-show="isShowBar">
            <div class="row border">
              <div class="col-4 my-auto">HTML</div>
              <div class="progress col-7 my-auto">
                <div class="html progress-bar progress-bar-striped progress-bar-animated" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" style="width: 75%"></div>
              </div>
            </div>
            <div class="row border">
              <div class="col-4 my-auto">CSS</div>
              <div class="progress col-7 my-auto">
                <div class="css progress-bar progress-bar-striped progress-bar-animated" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" style="width: 45%"></div>
              </div>
            </div>
            <div class="row border">
              <div class="col-4 my-auto">Javascript</div>
              <div class="progress col-7 my-auto">
                <div class="js progress-bar progress-bar-striped progress-bar-animated" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" style="width: 55%"></div>
              </div>
            </div>
            <div class="row border">
              <div class="col-4 my-auto">PHP</div>
              <div class="progress col-7 my-auto">
                <div class="php progress-bar progress-bar-striped progress-bar-animated" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" style="width: 65%"></div>
              </div>
            </div>
          </div>
        </div>
        
      <div class="bg-light otherskills my-5 py-3">
        <div class="h3 py-3 otherskills-title">other skills</div>
        <div class="row my-3">
          <div class="col-4">
            <font-awesome-icon :icon="['fas','laptop-code']" class="ml-5 text-dark skill-icon"/>
            <div class="border ml-5 mt-3 px-1 txt-skill">I'm into programming. I'm always thinking of something about it. Even if I'm free, I try to create something. However I don't think that it is studying, but just playing.</div>
          </div>
          <div class="col-4">
            <font-awesome-icon :icon="['fas','running']" class="text-dark skill-icon"/>
            <div class="border mx-3 mt-3 px-1 txt-skill">I have experienced to play some sports. For example, soccer, swimming, snowboard and dance. When I was a junior high school student, I was a captain of my soccer club and represnted Tokyo.</div>
          </div>
          <div class="col-4">
            <font-awesome-icon :icon="['fas','chalkboard-teacher']" class="mr-5 text-dark skill-icon"/>
            <div class="border mr-5 mt-3 px-1 txt-skill">I like to teach programming to someone who needs help. In fact, I often teach it my friends. Teaching is not only for friends, but also for me. I can understand more deeply through teaching.</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
.about {
  padding-bottom: 6rem;
}
.skills {
  padding-right: 30px;
  padding-left: 30px;
}
.skills-title {
  display: inline-block;
}
.html {
  background-color: coral;
}
.css {
  background-color: deeppink;
}
.js {
  background-color: darkseagreen;
}
.doughnat {
  height: 145px;
}
.skill-icon {
  font-size: 7em;
}
.txt-skill {
    display: inline-block;
    letter-spacing: .1em;
    text-align: start;    
}
</style>
<script>
import Doughnut from '../components/DoughnutChart.vue'
export default {
  components: {
    Doughnut
  },
  data: function() {
    return {
        isShowBar: false,
        isShowDoughnat: true,
        isShowHTML: true,
        isShowCSS: true,
        isShowJs: true,
        isShowPHP: true
      };
  },
  methods: {
    showBarChart: function() {
      this.isShowBar = true;
      this.isShowDoughnat = false;
    },
    showDoughnatChart: function() {
      this.isShowDoughnat = true;
      this.isShowBar = false;
    },
    toggleHTML: function() {
      if (this.isShowHTML) {
        this.isShowHTML = false;
      }else {
        this.isShowHTML = true;
      }
    },
    toggleCSS: function() {
      if (this.isShowCSS) {
        this.isShowCSS = false;
      }else {
        this.isShowCSS = true;
      }
    },
    toggleJs: function() {
      if (this.isShowJs) {
        this.isShowJs = false;
      }else {
        this.isShowJs = true;
      }
    },
    togglePHP: function() {
      if (this.isShowPHP) {
        this.isShowPHP = false;
      }else {
        this.isShowPHP = true;
      }
    },   
  }
}
</script>