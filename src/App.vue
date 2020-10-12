<template>
  <div>
    <headSiteContainer :title="'首页'"/>
    <h1>内容</h1>
  </div>
</template>

<script>
import headSiteContainer from './components/header/headSiteContainer';

export default {
  name: 'app',
  data() {
    return {

    }
  },
  components: {
    headSiteContainer
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