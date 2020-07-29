<template>
  <div>
    <form action="/">
      <van-search v-model="value"
        placeholder="请输入搜索关键词"
        @search="onSearch" />
    </form>

    <van-tabbar v-model="active"
      route>
      <van-tabbar-item replace
        to="/search"
        icon="search">搜索</van-tabbar-item>
      <van-tabbar-item icon="friends-o">标签</van-tabbar-item>
      <van-tabbar-item icon="setting-o">标签</van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script>
import { Toast } from "vant";

export default {
  name: "Home",
  data() {
    return {
      value: "",
      active: "",
    };
  },
  methods: {
    onSearch(val) {
      Toast(val);
    },
    onCancel() {
      Toast("取消");
    },
  },
};
</script>
