<script setup lang="ts">
import type { NavItem } from "@nuxt/content";

const navigation = inject<Ref<NavItem[]>>("navigation", ref([]));

const links = [
  {
    label: "About",
    to: "/about",
  },
  {
    label: "Services",
    to: "/services",
  },
  {
    label: "Testimonials",
    to: "/testimonials",
  },
  {
    label: "Patients",
    to: "/patients",
  },
  {
    label: "Providers",
    to: "/providers",
  },
  {
    label: "Contact",
    to: "/contact",
  },
];
</script>

<template>
  <AppBanner />
  <UHeader :links="links">
    <template #logo>
      <div class="flex items-center gap-2">
        <img
          class="w-auto h-12"
          src="/crg_full_logo.png"
          alt="Cheyenne Radiology"
        />
        Cheyenne Radiology
      </div>
    </template>

    <template #right>
      <UButton label="Schedule" color="gray" to="#" />
    </template>

    <template #panel>
      <UNavigationTree :links="mapContentNavigation(navigation)" default-open />
    </template>
  </UHeader>
</template>
