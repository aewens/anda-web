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
    /*border: 1px dashed rgba(255, 255, 255, 0.5);*/
    float: left;
    /*width: 20%;*/
    /*height: 100%;*/
    padding-right: 10px;
    overflow-x: hidden;
    overflow-y: scroll;
    scrollbar-width: none;
    background: var(--event-stream-background);
}
ul#event-stream li {
    width: 100%;
    margin: 5px;
    padding: 15px 5px;
    background: var(--event-stream-entry-background);
    color: var(--event-stream-entry-color);
    display: flex;
    justify-content: space-between;
}
ul#event-stream li p {
    display: inline-block;
    padding-right: 12px;
}
ul#event-stream li span {
    cursor: pointer;
    padding-right: 10px;
}

/*@media all and (max-width: 639px) {
    ul#event-stream {
        height: auto;
    }
}*/
</style>
