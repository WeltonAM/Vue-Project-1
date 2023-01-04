<template>
    <div id="center">
        <h1>Calculator VueJs</h1>
        <Calculator></Calculator>
    </div>
</template>

<script>
import Calculator from "./main/MyCalculator.vue"

export default {
    components: { Calculator }
}
</script>

<style>
    @font-face {
        font-family: "RobotoMono";
        src: url("./fonts/RobotoMono-Thin.ttf");
    }

    * {
        font-family: "RobotoMono", monospace;
    }

    body{
        margin: 0;
    }

    #app{
        display: flex;
        flex-direction: column;
        height: 100vh;
        justify-content: center;
        align-items: center;
        text-align: center;

        color: #fff;
        background: linear-gradient(to right, #3FB27F, #22303d);
    }

    #center{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    h1{
        animation: fairyLight 6s infinite;
    }

    @keyframes fairyLight {
        5% { color: red }
        10% { color: orange }
        25% { color: yellow }
        30% { color: green }
        40% { color: indigo }
        45% { color: violet }
        50% { color: red }
        55% { color: orange }
        60% { color: yellow }
        65% { color: green }
        75% { color: indigo }
        80% { color: violet }
        85% { color: red }
        90% { color: orange }
        95% { color: yellow }
        100% { color: green }
    }
</style>