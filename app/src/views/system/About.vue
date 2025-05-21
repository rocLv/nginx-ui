<script setup lang="ts">
import GithubButton from '@0xjacky/vue-github-button'
import logo from '@/assets/svg/icon.svg?url'
import ver from '@/version.json'

const thisYear = new Date().getFullYear()
</script>

<template>
  <ACard
    class="text-center"
    :bordered="false"
  >
    <div class="flex justify-center">
      <div class="logo">
        <div class="logo-container">
          <div class="image-bg" />
          <img
            class="image-src"
            :src="logo"
            alt="logo"
          >
        </div>
      </div>
    </div>
    <h2>北京云语</h2>
    <p>Yet another WebUI for Nginx</p>
    <p>Version: {{ ver.version }} ({{ ver.total_build || $gettext('Development Mode') }})</p>
   
    <p>Copyright © 2021 - {{ thisYear }} 北京云语 Team</p>
  </ACard>
</template>

<style lang="less" scoped>
.logo {
  position: relative;
  height: 256px;
  width: 256px;

  .image-bg {
    height: 120px;
    width: 120px;
    position: absolute;
    top: 50%;
    left: 50%;
    border-radius: 50%;
    filter: blur(72px);
    transform: translate(-50%, -50%);
    background-image: linear-gradient(-45deg, #3682D8 50%, #00D2FF 50%);
  }

  .image-src {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  img {
    max-width: 120px
  }
}
</style>
