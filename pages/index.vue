<template>
  <div id="app">
    <nav id="navbar">
        <header>
            <h1 onclick="">
                <span class="header-1">A</span>
                <span class="header-2">N</span>
                <span class="header-3">D</span>
                <span class="header-4">A</span>
            </h1>
        </header>
        <ul>
            <li><i class="fas fa-globe-americas icon-1" onclick=""></i></li>
            <li><i class="fas fa-globe-africa icon-2" onclick=""></i></li>
            <li><i class="fas fa-globe-europe icon-3" onclick=""></i></li>
            <li><i class="fas fa-globe-asia icon-4" onclick=""></i></li>
        </ul>
    </nav>
    <div id="viewports">
        <canvas>
        Canvas tag is not supported by this browser
        </canvas>
    </div>
    <footer id="footer">
        <p>FOOTER</p>
    </footer>
    <EventStream />
  </div>
</template>

<script>
import EventStream from "~/components/EventStream.vue"

export default {
  components: {
      EventStream
  }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    list-style-type: none;
}
#app {
    /*position: relative;*/
    /*width: 100%;*/
    height: 100vh;
    background: var(--base-background);
    color: var(--base-color);
    overflow: hidden;
    display: grid;
    grid-template-columns: 80% 20%;
    grid-template-rows: 4em 1fr 200px;
    grid-template-areas: "navbar navbar"
                         "viewports event-stream"
                         "footer event-stream";
}
#navbar {
    grid-area: navbar;
    background: var(--navbar-background);

    display: flex;
    justify-content: space-between;
    align-items: center;

    /*border: 1px dashed rgba(255, 255, 255, 0.5);*/
    box-shadow: rgba(36, 41, 51, 0.15) 0px 5px 10px 0px;
}
#navbar header {
    padding-left: 1em;
}
#navbar header h1 {
    /*font-size: 2em;*/
    cursor: pointer;
}
#navbar header h1:hover {
    cursor: pointer;
}
#navbar ul {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-right: 1em;
}
#navbar ul li {
    display: flex;
    padding-left: 2em;
}
#navbar ul li i {
    cursor: pointer;
    font-size: 1.25em;
}
#navbar ul li i:hover {
    cursor: pointer;
}
#viewports {
    grid-area: viewports;
    /*border: 1px dashed rgba(255, 255, 255, 0.5);*/
}
#footer {
    grid-area: footer;
    background: var(--footer-background);
    padding: 1em;
    /*border: 1px dashed rgba(255, 255, 255, 0.5);*/
}

.header-1 {
    color: var(--header-color-1);
}

.header-2 {
    color: var(--header-color-2);
}

.header-3 {
    color: var(--header-color-3);
}

.header-4 {
    color: var(--header-color-4);
}

#navbar header h1:hover .header-1 {
    color: var(--header-color-hover-1);
}

#navbar header h1:hover .header-2 {
    color: var(--header-color-hover-2);
}

#navbar header h1:hover .header-3 {
    color: var(--header-color-hover-3);
}

#navbar header h1:hover .header-4 {
    color: var(--header-color-hover-4);
}

.icon-1 {
    color: var(--icon-color-1);
}
.icon-1:hover {
    color: var(--icon-color-hover-1);
}

.icon-2 {
    color: var(--icon-color-2);
}
.icon-2:hover {
    color: var(--icon-color-hover-2);
}

.icon-3 {
    color: var(--icon-color-3);
}
.icon-3:hover {
    color: var(--icon-color-hover-3);
}

.icon-4 {
    color: var(--icon-color-4);
}
.icon-4:hover {
    color: var(--icon-color-hover-4);
}

@media all and (max-width: 639px) {
    #app {
        height: auto;
        grid-template-columns: auto;
        grid-template-rows: 4em 360px 240px auto;
        grid-template-areas: "navbar"
                             "viewports"
                             "footer"
                             "event-stream";
    }
}
</style>
