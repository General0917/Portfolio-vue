<template>
<div class="home">
  <div class="top container bg-light">
    Hello World.
  </div>
  <div class="bottom">
    <div class="mt-5 h4">
      Wellcome to my portfolio page!
    </div>
    <hr class="mb-5 mt-0 d-inline-block mx-auto" style="width: 27em;">
    <div class="container bg-light">
      <div class="my-3 py-3 px-2 txt border">
        These pages are mainly written in vue.js,  bootstrap4 and fontawesome.
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
// @ is an alias to /src

export default {
  name: 'home',
}
</script>
