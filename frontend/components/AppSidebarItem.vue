<script setup lang="ts">
defineProps<{
  title: string;
  description?: string;
}>();
</script>

<template>
  <li class="list-item">
    <div class="list-item-info">
      <p>{{ title }}</p>
      <span>{{ description }}</span>
    </div>
    <div class="ist-item-icons">
      <Icon name="uil:folder-open" class="list-item-icon" />
      <Icon name="uil:edit-alt" class="list-item-icon" />
      <Icon name="uil:trash-alt" class="list-item-icon" />
    </div>
  </li>
</template>

<style lang="scss" scoped>
.list-item {
  list-style: none;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  &:not(:first-child) {
    margin-top: 2rem;
  }
  &-icon {
    width: 30px;
    height: 30px;
    transition: background-color 0.1s ease-in-out;
    cursor: pointer;
    &:not(:first-child) {
      margin-left: 15px;
    }
    &:hover {
      background-color: rgba(0, 0, 0, 0.6);
    }
  }
  &-info {
    p {
      font-size: 20px;
    }
    span {
      font-size: 14px;
      color: rgba(0, 0, 0, 0.6);
    }
  }
}
</style>
