<script setup>
  import { ref, onMounted } from 'vue'
  import { RouterLink, RouterView } from 'vue-router'

  import ChevronUp from 'vue-material-design-icons/ChevronUp.vue';
  import ChevronDown from 'vue-material-design-icons/ChevronDown.vue';
  import ChevronLeft from 'vue-material-design-icons/ChevronLeft.vue';
  import ChevronRight from 'vue-material-design-icons/ChevronRight.vue';

  let openMenu = ref(false)
</script>

<template>
  <div class="">
    <div class="
      w-[calc(100%-240px)]
      h-[60px]
      fixed
      right-0
      z-20
      bg-[#101010]
      bg-opacity-80
      flex
      items-center
      justify-between
      "
    >
      <div class="flex items-center ml-6">
        <button type="button" class="rounded-full bg-black p-[1px] cursor-pointer">
          <ChevronLeft fillColor="#fff" :size="30"/>
        </button>
        <button type="button" class="rounded-full bg-black ml-4 p-[1px] cursor-pointer">
          <ChevronRight fillColor="#fff" :size="30"/>
        </button>
      </div>

      <button 
        @click="openMenu = !openMenu" :class="openMenu ? 'bg-[#282828]' : 'bg-black'"
        type="button"
        class="bg-black hover:bg-[#282828] rounded-full p-1 mr-8 mt-0.5 cursor-pointer"
      >
        <div class="flex items-center">
          <img src="https://yt3.ggpht.com/t-wTvZYsFlwjE-VRi1l_T78tq4fvNE-Wbgc7qFXq5gvYcvsFdpgj-JxEy7y4KpEGzCEQS2E79A=s88-c-k-c0x00ffffff-no-rj" class="rounded-full" width="27" alt="">
          <div class="text-white text-[14px] ml-1.5 font-semibold">BMhl</div>
          <ChevronDown fillColor="#fff" :size="25" v-if="!openMenu" @click="openMenu = true"/>
          <ChevronUp fillColor="#fff" :size="25" v-else @click="openMenu = false"/>
        </div>
      </button>
      <span
        v-if="openMenu"
        class="fixed w-[190px] bg-[#282828] rounded-sm shadow-2xl z-50 top-[52px] right-[35px] p-1 cursor-pointer"
      >
        <ul class="text-gray-200 font-semibold text-[14px]">
          <li class="border-g-gray-600 border-b hover:bg-[#3E3D3D] py-2.5 px-3">Profile</li>
          <li class="border-g-gray-600 border-b hover:bg-[#3E3D3D] py-2.5 px-3">Log out</li>
        </ul>
      </span>
    </div>
  </div>
</template>

