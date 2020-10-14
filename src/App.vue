<template>
  <div>
    <headSiteContainer :title="'首页'"/>
    <leftMenu />
  </div>
</template>

<script>
import headSiteContainer from './components/header/HeadSiteContainer';
import leftMenu from './components/leftMenu/LeftMenu';

export default {
  name: 'app',
  data() {
    return {

    }
  },
  components: {
    headSiteContainer,
    leftMenu
  }
}
</script>

<style lang="scss">
  html,body{
    overflow: hidden;
    padding: 0;
    margin: 0;
    height: 100%;
    width: 100%;
  }
</style>