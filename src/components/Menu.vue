<template>
  <div class="menu" :class="{ 'small-menu': smallMenu }">
    <MenuItem
      v-for="(item, index) in menuTree"
      :key="index"

      :data="item.children"
      :label="item.label"
      :icon="item.icon"
      :depth="0"
      
      :smallMenu="smallMenu"
      @click="toggle(item.link)"
    />
    <i @click="smallMenu = !smallMenu" class="material-icons">三</i>
  </div>
</template>

<script>
import MenuItem from './MenuItem.vue';
export default {
  name: 'recursive-menu',
  data: () => ({
    smallMenu: false,
    menuTree: [
      {
        label: "首頁",
        icon: "Home",
        link: "/home"
      },
      {
        label: "權限管理",
        icon: "Authorization",
        link: "/authorization"
      },
      {
        label: "資料查詢",
        icon: "Searching",
        link: "/search",
      }
    ]
  }),
  components: {
    MenuItem
  },  
  methods: {
    

    toggle(link) {
      if(link) {
        this.$router.push({ path: link })
      }
    },
  },
}
</script>

<style lang="scss" scoped>
.menu {
  position: fixed;
  height: 100vh;
  width: 240px;
  left: 0;
  top: 0;
  border-right: 2px solid #ececec;
  transition: all .3s ease;
  overflow: auto;
  background-color: #CECECE;
  i {
    position: fixed;
    left: 250px;
    font-size: 20px;
    top: 15px;
    user-select: none;
    cursor: pointer;
    transition: all .3s ease;
  }
  &.small-menu {
    overflow: inherit;
    width: 60px;
    padding-top: 50px;
    i {
      left: 20px;
    }
  }
}
</style>