<template>
    <header>
        <img @click="reload" src="@/assets/cashflow-icon.svg" alt="logo">
        <h1><span>Cash</span>Flow</h1>
        <span></span>
    </header>
</template>

<script>
export default {
    methods: {
        reload() {
            location.reload();
        },
    },
}
</script>

<style scoped>
header {
    display: flex;
    align-items: center;
    justify-content: space-around;
    width: 100vw;
}

img,
span {
    width: 48px;
}

h1 {
    color: var(--brand-blue);
}

h1 span {
    color: var(--brand-green);
}
</style>