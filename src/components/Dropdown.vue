<template>
    <div class="dropdown">
        <button class="btn btn-light dropdown-toggle"
                    type="button"
                    id="dropdownMenuButton"
                    data-toggle="dropdown"
                    aria-haspopup="true"
                    aria-expanded="false"
                    @click="toggleDropdown">
                    Menu
        </button>
        <div class="dropdown-menu" aria-labelledby="dropdownMenuButton" :class="{show: isDropdownOpen, 'dropdown-menu':true}">
            <li class="dropdown-item">
              <router-link to="/authorization" class="nav-link">權限管理</router-link>
            </li>
            <li class="dropdown-item">
              <router-link to="/search" class="nav-link">資料查詢</router-link>
            </li>
            <li class="dropdown-item">
              <router-link to="/profile" class="nav-link">個人資料</router-link>
            </li>
        </div>
    </div>
</template>

<script>
export default {
  name: "dropdownbutton",
  data() {
    return {}
  },
};
</script>

