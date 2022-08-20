<template>
    <canvas ref="gua" width="300" height="190"></canvas>
</template>
<script setup lang="ts">
const gua = ref(null);
let drawGua = function (canvas: HTMLCanvasElement) {
    let cxt = canvas.getContext("2d");
    cxt.fillStyle = "#dc3545"
    cxt.fillRect(50, 10, 200, 20)
    cxt.fillRect(50, 40, 200, 20)
    cxt.fillRect(50, 70, 200, 20)
    cxt.fillRect(50, 100, 200, 20)
    cxt.fillRect(50, 130, 200, 20)
    cxt.fillRect(50, 160, 200, 20)
}

onMounted(() => {
    drawGua(gua.value)
})


</script>
<style scoped>
canvas {
    width: 100%;
    min-width: 400px;
    height: 400px;
}
</style>