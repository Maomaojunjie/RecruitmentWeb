<template>
  <header class="header">
    <div class="container">
      <div class="header-inner">
        <div class="left-col">
          <ul class="nav nav-quick clearfix animated">
            <li v-for="navigationLink in leftLinks" :key="navigationLink.id">
              <nuxt-link :to="navigationLink.menuLink">{{
                navigationLink.menuName
              }}</nuxt-link>
            </li>
          </ul>
        </div>
        <div class="right-col">
          <ul class="nav nav-quick">
            <li v-for="navigationLink in rightLinks" :key="navigationLink.id">
              <nuxt-link :to="navigationLink.menuLink">{{
                navigationLink.menuName
              }}</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      leftLinks: [
        {
          id: '1',
          menuName: '首页',
          menuLink: '/'
        },
        {
          id: '2',
          menuName: '职位',
          menuLink: '/job'
        },
        {
          id: '3',
          menuName: '公司',
          menuLink: '/company'
        },
        {
          id: '4',
          menuName: '资讯',
          menuLink: '/news'
        }
      ],
      rightLinks: [
        {
          id: '1',
          menuName: '注册',
          menuLink: '/register'
        },
        {
          id: '2',
          menuName: '登录',
          menuLink: '/login'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
  border-bottom: 1px solid #f4f4f4;

  .nav {
  }
}
</style>
