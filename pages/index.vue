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
            <br />
            <div class="card mb-3">
                <div class="row g-0">
                    <div class="col-sm-4 bg-dark bg-gradient d-flex justify-content-center  align-items-center">
                       <diagram :yaoArrs="[true,true,true,true,true,true]"></diagram>
                    </div>
                    <div class="col-sm-8">
                        <div
                            class="card-body d-flex flex-column justify-content-start align-items-start fw-bold lh-base">
                            <span class="fs-1">乾【卦一】乾为天</span>
                            <span class="badge bg-secondary">原文</span>
                            <ul class="list-unstyled fs-6 ">
                                <li>乾。元，亨，利，贞</li>
                                <li>初九：潜龙勿用。</li>
                                <li>九二：见龙在田，利见大人。</li>
                                <li>九三：君子终日乾乾，夕惕若厉，无咎。</li>
                                <li>九四：或跃在渊，无咎。</li>
                                <li>九五：飞龙在天，利见大人</li>
                                <li>上九：亢龙有悔。</li>
                                <li>用九：见群龙无首，吉。</li>
                            </ul>
                            <span class="badge bg-secondary">《彖》曰</span>
                            <p>
                                大哉乾元！万物资始，乃统天。云行雨施，品物流形。大明终始，六位时成，时乘六龙以御天。乾道变化，各正性命。保合大和，乃利贞，首出庶物，万国咸宁。
                            </p>
                            <span class="badge bg-secondary">《象》曰</span>
                            <p>
                                天行，健。君子以自强不息。“潜龙勿用”， 阳在下也。“见龙在田”，德施普也。“终日乾乾”，反复道也。“或跃在渊”，进无咎也。“飞龙在天”，大人造也。“亢龙有悔”，
                                盈不可久也。“用九”，天德不可为首也。
                            </p>
                        </div>
                    </div>
                </div>
            </div>
            <br/>
            <div class="card mb-3">
                <div class="row g-0">
                    <div class="col-sm-4 bg-dark bg-gradient d-flex justify-content-center  align-items-center">
                        <diagram :yaoArrs="[false,false,false,false,false,false]"></diagram>
                    </div>
                    <div class="col-sm-8">
                        <div
                            class="card-body d-flex flex-column justify-content-start align-items-start fw-bold lh-base">
                            <span class="fs-1">坤【卦二】坤为地</span>
                            <span class="badge bg-secondary">原文</span>
                            <ul class="list-unstyled fs-6 ">
                                <li>坤元，亨。 利牝马之贞。君子有攸往，先迷后得主。利。西南得朋，东北丧朋。安贞吉。</li>
                                <li>初六：履霜，坚冰至。</li>
                                <li>六二：直方大。不习无不利。</li>
                                <li>六三：含章可贞。或从王事，无成有终。</li>
                                <li>六四：括囊。无咎无誉。</li>
                                <li>六五：黄裳。元吉。</li>
                                <li>上六：龙战于野。其血玄黄。</li>
                                <li>用六：利永贞。</li>
                            </ul>
                            <span class="badge bg-secondary">《彖》曰</span>
                            <p>
                               至哉坤元！万物资生，乃顺承天。坤厚载物，德合无疆。含弘光大，品物咸亨。“牝马”地类，行地无疆，柔顺利贞。“君子”攸行， 先迷失道， 后顺得常。“ 西南得朋”，乃与类行；“ 东北丧朋”，乃终有庆。“ 安贞”之“吉”，应地无疆。
                            </p>
                            <span class="badge bg-secondary">《象》曰</span>
                            <p>
                             地势，坤，君子以厚德载物。“ 履霜，坚冰”，阴始凝也。驯致其道，至坚冰也。六二之动，直以方也；“不习无不利”， 地道光也。“ 含章可贞”，以时发也。“或从王事”， 知光大也。“括囊无咎”， 慎不害也。“黄裳，元吉”，文在中也。“ 龙战于野”，其道穷也。“用六” 永贞，以大终也。
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>


    </div>
</template>
<script setup lang="ts">
import { Howl, Howler } from 'howler';
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