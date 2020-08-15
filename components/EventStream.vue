<template>
    <ul id="event-stream">
        <li v-for="entry in entries" :key="entry.id">
            <p>{{ entry.name }}</p>
            <span>+</span>
        </li>
    </ul>
</template>

<script>
export default {
    data() {
        return {
            entries: [
                {
                    name: "ENTRY",
                    data: {}
                },
                {
                    name: "ENTRY",
                    data: {}
                },
                {
                    name: "ENTRY",
                    data: {}
                },
                {
                    name: "ENTRY",
                    data: {}
                },
                {
                    name: "ENTRY",
                    data: {}
                }
            ]
        }
    }
}
</script>

<style scoped>
ul#event-stream {
    grid-area: event-stream;
    display: inline-block;
    border: 1px dashed rgba(255, 255, 255, 0.5);
    float: left;
    /*width: 20%;*/
    height: 100%;
    padding-right: 10px;
    overflow-x: hidden;
    overflow-y: scroll;
    scrollbar-width: none;
}
ul#event-stream li {
    display: block;
    width: 100%;
    margin: 5px;
    padding: 5px;
    border: 1px solid rgba(255, 255, 255, 0.5);
}
ul#event-stream li p {
    display: inline-block;
    padding-right: 12px;
}
ul#event-stream li span {
    position: absolute;
    width: 10px;
    right: 10px;
    cursor: pointer;
}
</style>
