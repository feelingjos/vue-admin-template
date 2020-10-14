<template>
  <div class="all-wrapper">
    <div class="slogan-wrapper">
      <div class="slogan-navbar-header">
        {{ titleName }}
      </div>
    </div>
    <div class="header-navbar-wrapper">
      <div class="retractable-icon">
        aa
      </div>
      <div class="level-menu-items">
        <div class="auto-level-menu-item-wrapper" >
          <div class="top-level-menu-item" v-for="one in data" :key="one">
            <div class="item-icon">icon{{one}}</div>
            <div class="item-title">title{{one}}</div>
          </div>
        </div>
      </div>
      <div class="header-profile-wrapper">
        profile
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeadSiteContainer',
  props: {
    title: String
  },
  data() {
    return {
      titleName: this.title,
      data: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20,
        21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40]
    }
  },
  methods: {
    goBack() {
      console.log('点击了标签')
    }
  }
}
</script>

<style lang="scss" scoped>
  .all-wrapper {
    height: 60px;
    width: 100%;
    //float:left;
    .slogan-wrapper {
      position: fixed;
      left: 0;
      top: 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 240px;
      height: 60px;
      z-index: 10;
      background-color: #FFDC45;
      padding: 0;
      box-sizing: border-box;
      .slogan-navbar-header{
        padding-left: 15px;
        height: 60px;
        line-height: 60px;
      }
    }
    .header-navbar-wrapper{
      //float: right;
      position: absolute;
      left: 240px;
      top:0;
      right: 0;
      //width: 100%;
      height: 60px;
      background: #76FF58;
      //overflow: auto;
      .retractable-icon{
        float: left;
        //display: inline-block;
        height: 60px;
        line-height: 60px;
        margin: 0 10px;
        cursor: pointer;
        width: 50px;
        background: blueviolet;
      }
      .level-menu-items{
        white-space: nowrap;
        //display: inline-block;
        height: 60px;
        background: aliceblue;
        line-height: 60px;
        cursor: pointer;
        margin: 0 auto;
        //position: relative;
        //padding: 0 10px;
        .auto-level-menu-item-wrapper{
          &:hover{
            overflow-x: auto;
            overflow-y: hidden;
          }
          //position: absolute;
          //top: 0;
          //bottom: 0;
          //right: 0;
          overflow: hidden;
          height: 60px;
          position: absolute;
          right: 270px;
          top: 0;
          left: 60px;
          .top-level-menu-item{
            display: inline-block;
            //float: left;
            background: azure;
            height: 60px;
            .item-icon{
              float: left;
            }
            .item-title{
              padding-left: 5px;
              float: left;
            }
          }
        }
      }
      .header-profile-wrapper{
        display: inline-block;
        position: absolute;
        right: 0;
        top: 0;
        background: cadetblue;
        width: 270px;
        height: 60px;
        line-height: 60px;
      }
    }
  }
</style>