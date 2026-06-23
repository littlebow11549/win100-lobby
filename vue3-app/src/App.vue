<template>
  <AppLayout
    :sidebar-collapsed="sidebarCollapsed"
    :mobile-sidebar-open="mobileSidebarOpen"
    @close-sidebar="mobileSidebarOpen = false"
  >
    <!-- 側邊欄 -->
    <template #sidebar>
      <!-- <Sidebar ... /> -->
      <div style="padding: 16px; color: #fff">Sidebar</div>
    </template>

    <!-- 頂部列 -->
    <template #header>
      <!-- <TopBar ... /> -->
      <div style="height: 64px; display:flex; align-items:center; padding: 0 24px; color:#fff">TopBar</div>
    </template>

    <!-- 頁面內容（預設 slot） -->
    <!-- <RouterView /> 或直接放頁面元件 -->
    <div style="color:#fff; padding: 24px 0">Content area</div>

    <!-- 頁尾 -->
    <template #footer>
      <!-- <AppFooter /> -->
    </template>

    <!-- 手機底部導覽 -->
    <template #mobile-nav>
      <!-- <MobileNav ... /> -->
    </template>
  </AppLayout>
</template>

<script setup>
import { ref } from 'vue';
import AppLayout from '@/layouts/AppLayout.vue';

const sidebarCollapsed  = ref(false);
const mobileSidebarOpen = ref(false);
</script>
