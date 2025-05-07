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
    
    </div>
  </div>
</template>

