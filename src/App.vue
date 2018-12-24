<template>
  <div id="app">
    <section class="system-layout">
      <section class="layout-header">
        <MainHeader/>
      </section>
      <section class="layout-main">
        <section class="layout-left">
          <MainNav/>
        </section>
        <section class="layout-right">
          <section class="layout-tab-head">

          </section>
          <section class="layout-tab-cont">
            <router-view/>
          </section>
        </section>
      </section>
    </section>
  </div>
</template>

<script>
import 'normalize.css';
import '@/styles/common.scss';
import MainHeader from '@/components/MainHeader';
import MainNav from '@/components/MainNav';

export default {
  components: {
    MainHeader,
    MainNav
  },
  watch: {
    $route() {
      console.log('aaa');
    }
  }
}
</script>

<style lang="scss">
.system-layout {
  position: relative;
  width: 100%;
  height: 100%;
  padding: 56px 0 0;
}
.layout-header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 56px;
}
.layout-main {
  display: table;
  position: relative;
  width: 100%;
  height: 100%;
}
.layout-left {
  display: table-cell;
  vertical-align: top;
  position: relative;
  width: 82px;
  height: 100%;
}
.layout-right {
  display: table-cell;
  vertical-align: top;
  position: relative;
  width: auto;
  height: 100%;
  padding-top: 41px;
}
.layout-tab-head {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.layout-tab-cont {
  position: relative;
  width: 100%;
  height: 100%;
}
</style>
