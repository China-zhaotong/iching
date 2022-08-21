<template>
    <div class="main">
        <nav class="navbar navbar-expand-lg sticky-top navbar-dark bg-dark bg-gradient">
            <div class="container-fluid">
                <tai-chi class="navbar-brand"></tai-chi>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent"
                    aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                        <!-- <li class="nav-item">
                            <a class="nav-link active" aria-current="page" href="#">《易经》</a>
                        </li> -->
                        <!-- <li class="nav-item">
                            <a class="nav-link" href="#">Link</a>
                        </li>
                        <li class="nav-item dropdown">
                            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                                data-bs-toggle="dropdown" aria-expanded="false">
                                Dropdown
                            </a>
                            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                                <li><a class="dropdown-item" href="#">Action</a></li>
                                <li><a class="dropdown-item" href="#">Another action</a></li>
                                <li>
                                    <hr class="dropdown-divider">
                                </li>
                                <li><a class="dropdown-item" href="#">Something else here</a></li>
                            </ul>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link disabled">Disabled</a>
                        </li> -->
                    </ul>
                </div>
            </div>
        </nav>
        <div class="container">
            <div class="card mb-3" v-for="item in iching" :key="item.title">
                <div class="row g-0">
                    <div class="col-sm-4 bg-dark bg-gradient d-flex justify-content-center  align-items-center">
                       <diagram :yaoArrs="item.yaoArrs"></diagram>
                    </div>
                    <div class="col-sm-8">
                        <div
                            class="card-body d-flex flex-column justify-content-start align-items-start fw-bold lh-base">
                            <span class="fs-1">{{item.title}}</span>
                            <span class="badge bg-secondary">原文</span>
                            <ul class="list-unstyled fs-6 ">
                                <li v-for="it in item.origin_cnt" :key="it">{{it}}</li>
                            </ul>
                            <span class="badge bg-secondary">《彖》曰</span>
                            <p>
                               {{item.tuan_cnt}}
                            </p>
                            <span class="badge bg-secondary">《象》曰</span>
                            <p>
                               {{item.xiang_cnt}}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>


    </div>
</template>
<script setup lang="ts">
import { Howl} from 'howler';

const { data: iching }:any = await useFetch('/json/iching.json')

//播放背景音乐
var sound = new Howl({
    src: ['mp3/bg.mp3'],
    html5: true
});



onMounted(() => {
    sound.play();

})
</script>
<style scoped>
.main {
    height: 100%;
}
</style>