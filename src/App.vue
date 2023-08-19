<template>
    <Suspense>
        <template #default>
            <Home />
        </template>
        <template #fallback>
            <SplashScreen />
        </template>
    </Suspense>
</template>

<script>
import SplashScreen from "@/components/SplashScreen.vue";
import { defineAsyncComponent } from "vue";

export default {
    components: {
        SplashScreen,
        // Lo que hacemos es cargar de manera asincrona el componente Home
        Home: defineAsyncComponent(() =>
            new Promise((resolve) => {
                setTimeout(() => {
                    resolve(import("./components/Home.vue"))
                }, 2500);
            })
        )
    },
};
</script>

<style>
html,
body,
.app {
    min-height: 100vh;
    margin: 0px;
    font-family: Arial, Helvetica, sans-serif;
}

* {
    --brand-green: #04b500;
    --brand-blue: #0689b0;
}
</style>
