<template>
  <section class="system-nav">
    <div class="main-nav">
      <NavList
        v-for="item in mainNavData"
        :key="item.code"
        :label="item.label"
        :child="item.child"
        :depth="0"
        :path="item.path"
      />
    </div>
  </section>
</template>

<script>
import NavList from '@/components/NavList';

export default {
  name: 'MainNav',
  components: {
    NavList
  },
  data() {
    return {
      mainNavData: [
        {
          code: '1',
          label: '宣传教育',
          path: '',
          child: [
            {
              code: '1-1',
              label: '宣传教育-主页',
              path: '/educat',
            },
            {
              code: '1-2',
              label: '宣传教育-课程列表',
              path: '/educat/list.html',
            }
          ]
        },
        {
          code: '2',
          label: '廉政档案',
          path: '/record'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  .system-nav {
    position: relative;
    width: 100%;
    height: 100%;
    background-color: $blue;
  }
</style>


