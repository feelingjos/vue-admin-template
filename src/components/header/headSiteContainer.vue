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
        <div class="top-level-menu-item">
          <div class="item-icon">icon1</div>
          <div class="item-title">title1</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon2</div>
          <div class="item-title">title2</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon3</div>
          <div class="item-title">title3</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon4</div>
          <div class="item-title">title4</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon5</div>
          <div class="item-title">title5</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon6</div>
          <div class="item-title">title6</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon7</div>
          <div class="item-title">title7</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon8</div>
          <div class="item-title">title8</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon9</div>
          <div class="item-title">title9</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon10</div>
          <div class="item-title">title10</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon11</div>
          <div class="item-title">title11</div>
        </div>
        <div class="top-level-menu-item">
          <div class="item-icon">icon12</div>
          <div class="item-title">title12</div>
        </div>
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
      titleName: this.title
    }
  },
  methods: {
    goBack() {
      console.log('点击了标签')
    }
  }
}
</script>

<style lang="scss">
  .all-wrapper {
    height: 60px;
    width: 100%;
    float:left;
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
      float: right;
      position: absolute;
      left: 240px;
      top:0;
      width: 100%;
      height: 60px;
      background: #76FF58;
      .retractable-icon{
        float: left;
        height: 60px;
        line-height: 60px;
        margin: 0 10px;
        cursor: pointer;
        width: 50px;
      }
      .level-menu-items{
        float: left;
        height: 60px;
        background: aliceblue;
        line-height: 60px;
        cursor: pointer;
        margin: 0 auto;
        padding: 0 10px;
        .top-level-menu-item{
          float: left;
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
  }
</style>