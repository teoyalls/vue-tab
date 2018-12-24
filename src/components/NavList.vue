<template>
  <div class="nav-list" :depth="depth + 1">
    <p class="nav-item" :title="label" :style="{'padding-left': getPaddingLeft}" @click="handle">
      <span class="nav-t">{{ label }}</span>
    </p>
    <NavList
      v-if="(child.length > 0)"
      v-for="item in child"
      :key="item.code"
      :label="item.label"
      :child="item.child"
      :depth="depth + 1"
      :path="item.path"
    />
  </div>
</template>

<script>
export default {
  name: 'NavList',
  props: [
    'label',
    'depth',
    'child',
    'path'
  ],
  computed: {
    getPaddingLeft() {
      return this.depth * 10 + 'px';
    }
  },
  methods: {
    handle() {
      if (this.path.length > 0) {
        this.$router.push(this.path);
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  .nav-list {
    position: relative;
    width: 100%;
    .nav-item {
      position: relative;
      width: 100%;
      height: 31px;
      border-bottom: 1px solid #21acfd;
      cursor: pointer;
    }
    .nav-t {
      line-height: 30px;
      color: #fff;
      white-space: nowrap;
    }
  }
</style>


