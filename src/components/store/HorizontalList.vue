<template>
    <div class="list-group">
        <!-- 单一窗格 -->
        <StandardItemFlow class="card" v-for="(item, index) in list" :key="index" :app="item"></StandardItemFlow>
    </div>
</template>

<script lang="ts" setup>
// import HorizontalCard from '@/components/store/HorizontalCard.vue'
import StandardItemFlow from '@/components/store/StandardItemFlow.vue'
import Application from '@/type/Application';
import { defineProps } from "vue";


defineProps<{
    list: Array<Application>,
}>()



</script>
<style>
.card {
    /* background: #000; */
    /* width: 30%; */
    float:right;
}

.list-group {
    /* width: 90%; */
    /* background: rgb(197, 245, 247); */
}
</style>
