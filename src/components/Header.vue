<template>
  <div class="header">
    <div clss="header-left">
      <el-dropdown>
        <span class="el-dropdown-link">
          <el-icon class="el-icon--right">
            <el-icon><Menu class="header-menu" /></el-icon>
          </el-icon>
        </span>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item>菜单一</el-dropdown-item>
            <el-dropdown-item>菜单二</el-dropdown-item>
            <el-dropdown-item>菜单三</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </div>

    <div class="header-right">
      <el-icon><User class="header-user" /></el-icon>
      <span>用户名</span>
    </div>
  </div>
</template>

<script lang="ts">
import { Menu, User } from "@element-plus/icons-vue";
export default {
  components: {
    Menu,
    User,
  },
  setup() {
    return {};
  },
};
</script>

<style lang="less" scoped>
.header {
  position: relative;
  top: 0;
  height: 20px;
  display: flex;
  justify-content: space-between;
  padding: 12px 16px;
  color: white;
  background: black;

  .header-menu {
    font-size: 18px;
    color: white;
  }

  .header-right {
    .header-user {
    }
  }
}
</style>

