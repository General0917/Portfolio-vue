<template>
  <div id="nav" class="footer bg-dark">
    <a href="https://twitter.com/shunya39836817" class="mx-1">
      <font-awesome-icon :icon="['fab','twitter']" class="text-light"/>
    </a>
    <a href="https://github.com/shunyaendoh1215" class="mx-1">
      <font-awesome-icon :icon="['fab','github']" class="text-light"/>
    </a>
    <a href="https://qiita.com/shunyaendoh" class="mx-1">
      <font-awesome-layers>
        <font-awesome-icon :icon="['fas','square']" class="text-light"/>
        <font-awesome-icon :icon="['fas','search']" transform="shrink-1" :style="{ color: 'black' }" />
      </font-awesome-layers>
    </a>
  </div>
</template>
<style>
.footer {
  opacity: 0.5;
}
</style>