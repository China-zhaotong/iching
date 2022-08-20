<template>
    <div class="main">
        <canvas ref="taiji" width="40" height="40"></canvas>
        <span><strong>《易经》</strong></span>
    </div>

</template>
<script setup lang="ts">
const taiji = ref(null);
/**
 * 画太极
 * @param canvas 
 */
let drawTaiJi = function (canvas: HTMLCanvasElement) {
    let cxt = canvas.getContext("2d");
    cxt.beginPath()
    cxt.arc(20, 20, 20, 90 * Math.PI / 180, 270 * Math.PI / 180)
    cxt.closePath()
    cxt.fillStyle = 'black'
    cxt.fill()

    cxt.beginPath()
    cxt.arc(20, 20, 20, 270 * Math.PI / 180, 90 * Math.PI / 180)
    cxt.closePath()
    cxt.fillStyle = 'white'
    cxt.fill()

    cxt.beginPath()
    cxt.arc(20, 10, 10, 0, 360 * Math.PI / 180)
    cxt.closePath()
    cxt.fillStyle = 'black'
    cxt.fill()

    cxt.beginPath()
    cxt.arc(20, 10, 3, 0, 360 * Math.PI / 180)
    cxt.closePath()
    cxt.fillStyle = 'white'
    cxt.fill()

    cxt.beginPath()
    cxt.arc(20, 30, 10, 0, 360 * Math.PI / 180)
    cxt.closePath()
    cxt.fillStyle = 'white'
    cxt.fill()


    cxt.beginPath()
    cxt.arc(20, 30, 3, 0, 360 * Math.PI / 180)
    cxt.closePath()
    cxt.fillStyle = 'black'
    cxt.fill()

}


onMounted(() => {
    drawTaiJi(taiji.value)
})
</script>
<style scoped>

.main{
    display: flex;
    flex-direction: row;
    align-items: center;
}

span {
    margin-left: 1rem;
}


canvas {
    animation: canvas_rorate 3s linear infinite;
}


@keyframes canvas_rorate {

    0% {
        -webkit-transform: rotate(0deg);
    }

    50% {
        -webkit-transform: rotate(180deg);
    }

    100% {
        -webkit-transform: rotate(360deg);
    }
}
</style>