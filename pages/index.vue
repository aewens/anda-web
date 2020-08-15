<template>
  <div id="app">
    <nav id="navbar">
        <header>
            <h1>ANDA</h1>
        </header>
        <ul>
            <li>HEADER</li>
            <li>HEADER</li>
            <li>HEADER</li>
            <li>HEADER</li>
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
    width: 100%;
    height: 100vh;
    background: #000;
    color: #fff;
    overflow: hidden;
    display: grid;
    grid-template-columns: 80% 20%;
    grid-template-rows: 50px 1fr 200px;
    grid-template-areas: "navbar navbar"
                         "viewports event-stream"
                         "footer event-stream";
}
#navbar {
    grid-area: navbar;
    background: #222;

    display: flex;
    justify-content: space-between;
    align-items: center;

    border: 1px dashed rgba(255, 255, 255, 0.5);
    /*box-shadow: 0 4px 6px 0px rgba(255, 255, 255, 0.5);*/
}
#navbar header {
    padding-left: 1em;
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
#viewports {
    grid-area: viewports;
    border: 1px dashed rgba(255, 255, 255, 0.5);
}
#footer {
    grid-area: footer;
    background: #111;
    padding: 1em;
    border: 1px dashed rgba(255, 255, 255, 0.5);
}

@media all and (max-width: 639px) {
    #app {
        grid-template-columns: auto;
        grid-template-rows: 50px 1fr 200px 1fr;
        grid-template-areas: "navbar"
                             "viewports"
                             "footer"
                             "event-stream";
    }
}
</style>
