<template>
  <div class="demo">
    <header style="height: 300px; background-color: #333;color: #fff">I am header</header>

    <wmui-scrollspy 
    :panelNavs="panelNavs" 
    :hasBackTop="true" 
    defaultNav="首页">
      <div class="wmui-scrollspy-panel">
        <p class="one">one</p>
      </div>
      <div class="wmui-scrollspy-panel">
        <p class="two">two</p>
      </div>
      <div class="wmui-scrollspy-panel">
        <p class="three">three</p>
      </div>
    </wmui-scrollspy>

    <footer style="height: 300px; background-color: #333; color: #fff;">I am footer </footer>
  </div>
</template>
<script>

export default {
  data () {
    return {
      panelNavs: ['一楼', '二楼', '三楼']
    }
  }
}
</script>
<style lang="scss">
// 导航
.wmui-scrollspy-navs {
  position: fixed;
  bottom: 50px;
  right: 50px;
  ul {
    background-color: #eee;
    li {
      width: 50px;
      height: 50px;
      line-height: 50px;
      text-align: center;
    }
  }
}

// 高亮
.wmui-scrollspy-active {
  background-color: gray !important;
}

// 自定义，不需要设置高度
.one,
.two,
.three {
  font-size: 60px;
  width: 100%;
  padding-top: 100px;
  text-align: center;
}
.one {
  background: green;
  padding-bottom: 200px;
}
.two {
  padding-bottom: 500px;
  background: teal;
}
.three {
  padding-bottom: 400px;
  background: red;
}
</style>
