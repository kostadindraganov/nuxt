<template>
    <div ref="splineContainer" style="width: 100%; height: 600px;"></div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue'
  import { Viewer } from '@splinetool/viewer'
  
  const splineContainer = ref(null)
  
  onMounted(() => {
    const viewer = new Viewer({
      container: splineContainer.value,
      url: 'https://prod.spline.design/P2ZU0z99Lip0dQHu/scene.splinecode' // Replace with your Spline JSON URL
    })
  
    viewer.on('loaded', () => {
      console.log('Spline loaded successfully')
    })
  })
  </script>
  
  <style scoped>
  /* Add custom styles if needed */
  </style>