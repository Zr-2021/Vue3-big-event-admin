<script setup lang="ts">
import { useUserStore } from '@/stores/user'
const userStore = useUserStore()
</script>

<template>
  <router-view></router-view>
  {{ userStore.token }}
  <el-button
    type="primary"
    @click="userStore.setToken('shfjkdshafjkdshajklfds')"
    >登录</el-button
  >
  <el-button type="success" @click="userStore.setToken('')">退出</el-button>
</template>

<style scoped></style>
