<template>
    <div class="menu-left-wrapper">
        <div class="menu-left-context">
            menu-left-context
        </div>
        <div class="main-context-wrapper">
            main-context-wrapper
        </div>
    </div>
</template>

<script>
export default {
  name: 'LeftMenu'
}
</script>

<style lang="scss" scoped>
    .menu-left-wrapper{
       background: #379e78;
       position: absolute;
       top: 60px;
       right: 0;
       bottom: 0;
       height: 100%;
       width: 100%;
       .menu-left-context{
           background: blue;
           position: absolute;
           //top: 60px;
           left: 0;
           bottom: 0;
           height: 100%;
           width: 240px;
       }
       .main-context-wrapper{
           background: #27a7ff;
           position: absolute;
           //top: 60px;
           left: 240px;
           right: 0;
           bottom: 0;
           height: 100%;
           width: 100%;
       }
    }
</style>