<template>
  <div class="w-screen min-h-screen bg-primary">

    <div class="min-h-screen flex flex-col justify-center items-center gap-3">
      <div><img :src=image></div>
      <h1  class="text-white font-semibold text-4xl mb-4">Welcome!</h1>
      <div class="flex gap-5">
        <Button @click="navigateTo('https://project-3-full-stack-agile-web-902-team-3-ox1o.onrender.com/')">Project Docs</Button> 
        <Button @click="navigateTo('DJANGO URL')">Django Docs</Button> 
      </div>
    </div>
  </div>
</template>

<script>
import logo from "@/assets/revs_logo.webp";
import Button from "@/components/PrimaryButton.vue"

export default {
  components: {
    Button
  },
  methods: {
    navigateTo(route) {
      window.open(route, '_blank')
    },
  },

  data() {
    return {
      image: logo,
    };
  },
};
</script>
