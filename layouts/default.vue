<template>
  <div>
    <nuxt />
  </div>
</template>

<script>
if (/iPad|iPhone|iPod/.test(navigator.userAgent)) {
    window.document.addEventListener("touchmove", e => {
        if(e.scale !== 1) {
            e.preventDefault();
        }
    }, {passive: false});
}
</script>

<style>
html {
  /*font-size: 16px;*/
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background: #000;
}
</style>
