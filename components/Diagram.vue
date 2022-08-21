<template>
    <canvas ref="gua" width="300" height="190"></canvas>
</template>
<script setup lang="ts">
const gua = ref(null);

const props = defineProps({
    yaoArrs: { type: Array, required: true },
})
let drawGua = function (canvas: HTMLCanvasElement) {
    let cxt = canvas.getContext("2d");
    props.yaoArrs.forEach((item, index) => {
        if (item) {
            cxt.fillStyle = "#dc3545"
            cxt.fillRect(50, 10 + 30 * index, 200, 20)
        } else {
            cxt.fillStyle = "#dc3545"
            cxt.fillRect(50, 10 + 30 * index, 90, 20)
            cxt.fillRect(160, 10 + 30 * index, 90, 20)
        }
    })
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