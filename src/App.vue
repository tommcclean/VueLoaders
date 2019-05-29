<template>
    <div id="vueloaders">
        <section>
            <h2>Loading container</h2>
            <p>Use the loading container to show a spinner while your content is loading. Inject your content using the default slot.</p>
            <div class="left">
                <loading-container :is-loading="true">
                    <p slot="loader">Is loading</p>
                    <p slot="content">Is NOT loading</p>
                </loading-container>
            </div>
            <div class="right">
                <loading-container :is-loading="false">
                    <p slot="loader">Is loading</p>
                    <p slot="content">Is NOT loading</p>
                </loading-container>
            </div>
        </section>

        <section>
            <h2>Loading button</h2>
            <p>Use the loading button to prevent a user from clicking a submitted form, and to show the user something is happening once clicked.</p>
            <div class="left">
                <loading-button :is-loading="true" text="Submit">
                    <span>[ Is Loading ]</span>
                </loading-button>
            </div>
            <div class="right">
                <loading-button :is-loading="false" text="Submit">
                    <span>[ Is Loading ]</span>
                </loading-button>
            </div>
        </section>
    </div>
</template>

<script>
import "@/components/index.js";

export default {
    name: "vuestack",
    data() {
        return {
            showAppPanelLeft: false,
            showAppPanelRight: false,
            showNotificationPanel: false
        };
    }
};
</script>

<style scoped>
#vueloaders {
    font-family: sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

section {
    border-bottom: 1px solid black;
    background-color: whitesmoke;
    padding: 10px;
    padding-bottom: 20px;
}

section::after {
    visibility: hidden;
    display: block;
    font-size: 0;
    content: " ";
    clear: both;
}

section .left {
    float: left;
    width: calc((100% - 44px) / 2);
    padding: 10px;
    border: 1px dashed gray;
}

section .right {
    float: right;
    width: calc((100% - 44px) / 2);
    padding: 10px;
    border: 1px dashed gray;
}
</style>
