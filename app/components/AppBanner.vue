<template>
  <div class="bg-primary py-3 text-white">
    <div class="container m-auto pa-1">
      <div class="flex items-center justify-center lg:justify-between">
        <div class="flex items-center gap-2 lg:gap-6">
          <div class="flex items-center gap-2">
            <Icon name="i-heroicons-envelope" />
            <a href="mailto:scheduling@cheyrad.com" class="text-small">
              Email Us
            </a>
          </div>
          <div class="flex items-center gap-2">
            <Icon name="i-heroicons-phone" />
            <a href="tel:+1-800-123-4567" class="text-small"> Call Us </a>
          </div>
        </div>
        <ul class="hidden items-center divide-x divide-white text-base lg:flex">
          <li class="px-3">Follow Us</li>
          <li class="flex items-center px-3">
            <a href="#">
              <UIcon
                class="hover:text-secondary text-base transition"
                name="i-bi-facebook"
              />
            </a>
          </li>
          <li class="flex items-center px-3">
            <a href="#">
              <UIcon
                class="hover:text-secondary text-base transition"
                name="i-bi-linkedin"
              />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style></style>
