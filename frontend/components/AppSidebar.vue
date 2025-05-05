<script setup lang="ts">
const items = [
  {
    title: "サンプル１",
    description: "初めのロードマップです。",
  },
  {
    title: "サンプル２",
    description: "初めのロードマップです。",
  },
  {
    title: "サンプル３",
    description: "初めのロードマップです。",
  },
  {
    title: "サンプル４",
    description: "初めのロードマップです。",
  },
];
</script>

<template>
  <div class="sidebar">
    <h2 class="header">
      <span>ロードマップ一覧</span
      ><Icon name="uil:angle-double-left" class="header-icon" />
    </h2>
    <ul class="list">
      <template v-for="item in items" :key="item.title">
        <AppSidebarItem :title="item.title" :description="item.description" />
      </template>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.sidebar {
  width: 400px;
  border-right: 1px solid rgba(0, 0, 0, 0.2);
  padding: 1rem 1.5rem;

  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 1rem;
    border-bottom: 1px solid rgba(0, 0, 0, 0.2);
    span {
      font-size: 1.2rem;
    }
    &-icon {
      width: 40px;
      height: 40px;
      transition: background-color 0.1s ease-in-out;
      cursor: pointer;
      &:hover {
        background-color: rgba(0, 0, 0, 0.6);
      }
    }
  }

  .list {
    height: calc(100% - 200px);
    padding: 0;
    margin-top: 2rem;
    /* TODO */
    /* overflow: scroll;
    &::-webkit-scrollbar {
      display: none;
    } */
  }
}
</style>
