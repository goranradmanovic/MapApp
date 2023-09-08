<script setup>
  import IconHouse from '@/components/icons/IconHouse.vue'
  import IconInfo from '@/components/icons/IconInfo.vue'
  import { RouterLink } from 'vue-router'

  const toggleMenu = event => event.srcElement.parentElement.classList.toggle('shrink')
</script>

<template>
  <aside>
    <button class="menu__btn" @click="toggleMenu($event)">☰</button>
    <ul>
      <li>
        <IconHouse title="Home" />
        <RouterLink to="/">
          <span>Home</span>
        </RouterLink>
      </li>
      <li>
        <IconInfo title="About" />
        <RouterLink to="/about">
          <span>About</span>
        </RouterLink>
      </li>
    </ul>
  </aside>
</template>
