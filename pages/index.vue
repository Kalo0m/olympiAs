<template>
  <div
    class="container mx-auto px-4 max-w-full bg-gray-800 h-screen/2 flex justify-center items-center flex-col"
  >
    <div class="relative overflow-hidden h-1/2 w-full">
      <transition name="image" appear-active-class="aa-enter-active" appear>
        <img
          src="~/assets/img/logoOlympias.png"
          alt="aaa"
          class="h-full w-full object-contain absolute"
        />
      </transition>
    </div>
    <transition name="text" appear-active-class="up-text" appear>
      <p class="font-sans text-3xl font-light text-gray-300">
        Ravivons la flamme
      </p>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
    }
  },
}
</script>

<style>
.aa-enter-active {
  animation: go 2s;
}

@keyframes go {
  from {
    opacity: 0;
  }
  to {
    background: 1;
  }
}
.up-text {
  animation: up-text 3s;
}

@keyframes up-text {
  from {
    transform: translate(-50px, 0px);
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
