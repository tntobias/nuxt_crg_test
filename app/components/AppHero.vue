<template>
  <div class="w-screen overflow-x-hidden">
    <header class="relative h-screen bg-cover bg-no-repeat bg-[url(/hero.png)]">
      <div
        class="flex h-full items-center bg-gradient-to-r from-primary to-transparent text-white"
      >
        <div class="container m-auto">
          <div class="lg:w-8/12">
            <h1 class="font-bold text-6xl aos-init aos-animate">
              {{ props.title }}
            </h1>

            <p class="mb-12 mt-8 text-xl">
              {{ props.description }}
            </p>

            <div class="flex items-center gap-2">
              <UButton
                v-for="link in props.links"
                :key="link.to"
                :label="link.label"
                color="gray"
                :to="link.to"
              />
            </div>
          </div>
        </div>
      </div>
    </header>
    <div class="container m-auto relative">
      <div
        class="static -top-20 grid grid-cols-1 gap-4 bg-white p-7 shadow-[0_3px_32px_0_#0067FF1A] md:grid-cols-2 lg:absolute lg:grid-cols-3 lg:p-14"
      >
        <aside
          class="flex flex-col items-center justify-center gap-6 text-center text-dark lg:flex-row lg:text-left"
        >
          <UIcon name="i-heroicons-clipboard" class="text-primary text-8xl" />
          <aside>
            <h3 class="text-2xl font-medium text-dark">MRI</h3>
            <p class="text-gray-dark">
              CRG has two state of the art MRI machines.
            </p>
          </aside>
        </aside>
        <aside
          class="flex flex-col items-center justify-center gap-6 text-center text-dark lg:flex-row lg:text-left"
        >
          <UIcon name="i-heroicons-heart" class="text-primary text-8xl" />
          <aside>
            <h3 class="text-2xl font-medium text-dark">Ultrasound</h3>
            <p class="text-gray-dark">We do ultrasound as well!</p>
          </aside>
        </aside>
        <aside
          class="flex flex-col items-center justify-center gap-6 text-center text-dark lg:flex-row lg:text-left"
        >
          <UIcon name="i-ph:pulse-fill" class="text-primary text-8xl" />
          <aside>
            <h3 class="text-2xl font-medium text-dark">PET/CT</h3>
            <p class="text-gray-dark">We pretty much rule at everything...</p>
          </aside>
        </aside>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const props = defineProps<{
  title: string;
  description: string;
  links: { label: string; to: string }[];
}>();
</script>

<style></style>
