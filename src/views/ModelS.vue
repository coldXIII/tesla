<script setup>
import { useModelSStore } from '../store/model_s';
import Intro from '@/components/Intro.vue';
import Interior from '@/components/Interior.vue';
import Grid from '@/components/Grid.vue';
import InterSection from '../components/InterSection.vue';
import ImageTabs from '../components/ImageTabs.vue'
import VideoTabs from '../components/VideoTabs.vue'
import ImageSection from '@/components/ImageSection.vue';
import Specs from '../components/Specs.vue';
import Video from '@/components/Video.vue';
import VideoSection from '@/components/VideoSection.vue';

const store = useModelSStore();
</script>

<template>
  <div class="min-h-screen w-screen">
    <Intro :store="store.intro" />
    <Interior :store="store.interior" />
    <Video :store="store.videoSlider" />
    <Grid :store="store.grid" />
    <InterSection :store="store.ludicrous" />
    <ImageTabs :store="store.tabs" />
    <InterSection :store="store.designed" />
    <Grid :store="store.grid2" />
    <VideoSection :store="store.videoSection" />
    <ImageTabs :store="store.maps" />
    <ImageSection :store="store.imageSection" />
    <InterSection :store="store.future" :marker="'future'" />
    <VideoTabs :store="store.autopilot" />
        <Specs :store="store.specs" />
  </div>
</template>
