<template>
  <div>
    <div class="footer">
      <van-tabbar v-model="active">
        <van-tabbar-item
          :icon="item.ico"
          :to="item.path"
          v-for="(item, index) in list"
          :key="index"
          >{{ item.title }}</van-tabbar-item
        >
      </van-tabbar>
    </div>
    <router-view v-wechat-title="$route.meta.title"></router-view>
  </div>
</template>
<script>
export default {
  data() {
    return {
      active: 0,
      list: [
        { title: "首页", path: "/index", ico: "wap-home-o" },
        { title: "分类", path: "/class", ico: "qr" },
        { title: "购物车", path: "/cart", ico: "shopping-cart-o" },
        { title: "我的", path: "/my", ico: "contact" }
      ]
    };
  }
};
</script>
