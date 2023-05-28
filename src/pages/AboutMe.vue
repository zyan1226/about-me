<template>
  <div>
    <!-- <div class="fixed right-32 bottom-24">
      <a>下载简历</a>
    </div> -->
    <div id="box" class="lg:w-7/12 sm:w-9/12 bg-white sm:mx-auto sm:my-20 mx-5 sm:p-20
         p-10 rounded-3xl break-words my-5 shadow-xl ring-1 ring-gray-900/5 opacity-95 backdrop-blur-3xl">
      <div class="flex sm:flex-row items-center flex-col">
        <img src="../assets/avatar.png" alt="" class="w-full sm:hidden">
        <p class="text-5xl font-semibold">{{ modelData.name }}</p>
        <img src="../assets/avatar.png" alt="" class="w-14 h-14 ml-auto hidden sm:inline-block">
      </div>
      <div class="mt-4 flex flex-row items-center flex-wrap">
        <a class="link red-link" href="https://blog.zyan1226.cn">博客</a>
        <a class="link green-link" href="https://juejin.cn/user/3702810895726344/posts">掘金</a>
        <a class="link purple-link" href="https://gitee.com/zyan1226">Gitee</a>
        <a class="link rose-link" href="https://github.com/zyan1226">GitHub</a>
        <a class="link gray-link" href="https://unsplash.com/@zyan1226">Unsplash</a>
        <a class="link red-link" href="https://space.bilibili.com/124493907">bilibili</a>
      </div>
      <div v-for="item in modelData.content" :key="item.title">
        <p class="text-2xl font-semibold mt-10">{{ item.title }}</p>
        <p class="mt-5 text-lg" v-for="(contentItem, index) in item.content" :key="index">{{ contentItem }}</p>
      </div>
      <p class="text-center mt-20 text-sm text-gray-500">
        Copyright © 2023 zyan. 保留所有权利。
      </p>
    </div>
  </div>
</template>

<script>
import { ModelData } from '../model/ModelData'

export default {
  name: 'AboutMe',
  data() {
    return {
      modelData: ModelData
    }
  }
}
</script>

<style scoped>
@keyframes upAnimation {
  0% {
    margin-top: 20rem;
  }
}

#box {
  animation-name: upAnimation;
  animation-duration: 2s;
  animation-iteration-count: 1;
}

.link {
  @apply text-lg px-3 py-2 font-semibold rounded-md mr-3 mt-3;
  transition: 750ms;
}

.red-link {
  color: #fc3549;
  background-color: #ffebed;
}

.red-link:hover {
  color: white;
  background-color: #e84950;
  transition: 750ms;
}

.green-link {
  color: #22a3ab;
  background-color: #dcfdff;
}

.green-link:hover {
  color: white;
  background-color: #68d9e5;
  transition: 750ms;
}

.purple-link {
  color: #7735fc;
  background-color: #e4dafc;
}

.purple-link:hover {
  color: white;
  background-color: #6f39f2;
  transition: 750ms;
}

.rose-link {
  color: #ed00d4;
  background-color: #f8d7f2;
}

.rose-link:hover {
  color: white;
  background-color: #d92fcd;
  transition: 750ms;
}

.gray-link {
  color: #888888;
  background-color: #f3f3f3;
}

.gray-link:hover {
  color: white;
  background-color: #888888;
  transition: 750ms;
}
</style>
