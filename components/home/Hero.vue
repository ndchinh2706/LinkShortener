<script setup>
import { AreaChart } from 'lucide-vue-next'
import { GitHubIcon } from 'vue3-simple-icons'

const { title, description, github } = useAppConfig()
</script>

<template>
  <main
    class="grid pt-8 pb-8 lg:grid-cols-2 place-items-center md:py-12"
  >
    <div>
      <h1
        class="text-5xl font-bold lg:text-6xl xl:text-7xl lg:tracking-tight xl:tracking-tighter"
      >
        {{ title }}
      </h1>
      <p class="max-w-xl mt-4 text-lg text-slate-600">
        {{ description }}
      </p>
      <div class="flex flex-col gap-3 mt-6 sm:flex-row">
        <HomeLink
          href="/dashboard"
          target="_blank"
          title="Đi uống bia"
          class="flex items-center justify-center gap-1"
          rel="noopener"
        >
          <AreaChart
            class="w-5 h-5"
          />
          Đi uống bia
        </HomeLink>
      </div>
    </div>
    <div class="hidden py-6 md:block">
      <img
                src="https://blog.dktcdn.net/files/mo-quan-bia-hoi.jpg"
                :alt="uongbeer"
                class="w-[512px]"
              >
    </div>
  </main>
</template>
