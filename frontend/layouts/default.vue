<script setup lang="ts"></script>

<template>
  <div>
    <!-- headerの読み込み -->
    <AppHeader />

    <!-- mainの読み込み -->
    <main>
      <AppSidebar />
      <slot />
    </main>

    <!-- footerの読み込み -->
    <AppFooter />
  </div>
</template>

<style lang="scss">
main {
  /* header、footerのheightを考慮 */
  min-height: calc(100vh - (40px + 2rem) - (10px + 2rem));
  width: 100%;
  display: flex;
}
</style>
