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
:root {
    --polar-night-darker: var(--nord0);
    --polar-night-dark: var(--nord1);
    --polar-night-light: var(--nord2);
    --polar-night-lighter: var(--nord3);
    --snow-storm-dark: var(--nord4);
    --snow-storm: var(--nord5);
    --snow-storm-light: var(--nord6);
    --frost-lighter: var(--nord7);
    --frost-light: var(--nord8);
    --frost-dark: var(--nord9);
    --frost-darker: var(--nord10);
    --aurora-red: var(--nord11);
    --aurora-orange: var(--nord12);
    --aurora-yellow: var(--nord13);
    --aurora-green: var(--nord14);
    --aurora-purple: var(--nord15);

    --base-background: var(--polar-night-light);
    --base-color: var(--snow-storm);

    --navbar-background: rgb(36, 41, 51);
    --header-color-1: var(--aurora-purple);
    --header-color-2: var(--aurora-red);
    --header-color-3: var(--aurora-orange);
    --header-color-4: var(--aurora-yellow);
    --header-color-hover-1: var(--frost-darker);
    --header-color-hover-2: var(--frost-dark);
    --header-color-hover-3: var(--frost-light);
    --header-color-hover-4: var(--frost-lighter);
    --icon-color-1: var(--aurora-yellow);
    --icon-color-2: var(--aurora-orange);
    --icon-color-3: var(--aurora-red);
    --icon-color-4: var(--aurora-purple);
    --icon-color-hover-1: var(--frost-lighter);
    --icon-color-hover-2: var(--frost-light);
    --icon-color-hover-3: var(--frost-dark);
    --icon-color-hover-4: var(--frost-darker);

    --footer-background: var(--polar-night-dark);

    --event-stream-background: var(--polar-night-darker);
    --event-stream-entry-background: var(--polar-night-lighter);
    --event-stream-entry-color: var(--snow-storm-dark);
}

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
