<template>
    <div class="menu-left-wrapper">
        <div class="menu-left-context">
            <!--<div class="menu-context-item-list">-->
                <div class="menu-left-nav" v-html="html">
                    <!--<div class="menu-left-itme">
                        菜单一
                    </div>-->
                </div>
            <!--</div>-->

        </div>
        <div class="main-context-wrapper">
            main-context-wrapper
        </div>
    </div>
</template>

<script>
export default {
  name: 'LeftMenu',
  data: function() {
    return {
      html: '',
      d: 10,
      menuData: [
        {
          title: 1,
          children: [
            {
              title: '1-1'
            },
            {
              title: '1-2'
            },
            {
              title: '1-3',
              children: [
                {
                  title: '1-3-1'
                },
                {
                  title: '1-3-2'
                },
                {
                  title: '1-3-3'
                }
              ]
            }
          ]
        }/*,
        {
          title: 2
        },
        {
          title: 3
        },
        {
          title: 4
        },
        {
          title: 5,
          children: [
            {
              title: '5-1'
            },          
            {           
              title: '5-2'
            },         
            {          
              title: '5-3'
            }
          ]
        },
        {
          title: 6,
          children: [
            {
              title: '6-1'
            },        
            {         
              title: '6-2',
              children: [
                {
                  title: '6-2-1'
                },
                {
                  title: '6-2-2'
                },
                {
                  title: '6-2-3'
                }
              ]
            },        
            {         
              title: '6-3'
            }
          ]
        } */
      ]
    };
  },
  created: function() {
    this.renderLeftMnue()
  },
  methods: {
    renderLeftMnue: function() {
      function renderChildren(datac) {
        for (let i = 0; i < datac.length; i++) {
          // debugger
          // let left = data[i]
          console.log('index', i, datac[i].title)
          var Mnue = `<div class="menu-left-item">
                    ${datac[i].title}

                    ${datac[i].children ? renderChildren(datac[i].children, leftMnueHtml) : ''}

                    </div>`

          leftMnueHtml += Mnue;
          // htmldata += Mnue;

          if (datac[i].children && datac[i].children.length > 0) {
            renderChildren(datac[i].children, leftMnueHtml)
          }
        }
        return leftMnueHtml
      }

      var leftMnueHtml = ''
      var data = this.menuData;

      for (let i = 0; i < data.length; i++) {
        // let left = data[i]
        console.log('index', i, data[i].title)
        var Mnue = `<div class="menu-left-itme">
                    ${data[i].title}

                    </div>`

        leftMnueHtml += Mnue;

        if (data[i].children && data[i].children.length > 0) {
          renderChildren(data[i].children, leftMnueHtml)
          // console.log(leftMnueHtml)
        }
        // leftMnueHtml += Mnue;
      }
      this.html = leftMnueHtml;
    }
  }
}
</script>

<style lang="scss" scoped>
    .menu-left-wrapper{
       //background: #379e78;
       position: absolute;
       top: 60px;
       right: 0;
       bottom: 0;
       height: 100%;
       width: 100%;
       .menu-left-context{
           //background: blue;
           position: absolute;
           //top: 60px;
           top: 0;
           left: 0;
           bottom: 0;
           //bottom: 60px;
           //height: 100%;
           width: 240px;
           .menu-left-nav{
               position: absolute;
               bottom: 60px;
               left: 0;
               top: 0;
               overflow: auto;
               width: 240px;
               //position: absolute;
               ::v-deep .menu-left-item{
                   background: azure;
                   padding: 10px ;
                   height: 50px;
               }
           }
           /*.menu-context-item-list{
               //position: absolute;
               //bottom: 0;
               //left: 0;
               //top: 0;
               width: 240px;
               //height: 100%;
               background: #cd21ff;
           }*/

       }
       .main-context-wrapper{
           //background: #27a7ff;
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