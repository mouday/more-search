<template>
  <div class="search">
    <iframe :src="currentUrl"
      frameborder="0"
      @load="handleChange"></iframe>
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
      currentUrl: "https://www.baidu.com/",
    };
  },

  watch: {
    currentUrl(val) {
      console.log(val);
    },
  },

  methods: {
    onSearch(val) {
      Toast(val);
    },
    onCancel() {
      Toast("取消");
    },

    handleChange(val) {
      console.log(val);
      //       var url = obj.contentWindow.location.href;
      // if(url.indexOf("bizOrderId") != -1) {
      // console.log(url);
    },
  },
};
</script>

<style lang="scss" scoped>
.search {
  width: 100%;
  height: 100%;
}

iframe {
  width: 100%;
  height: 100%;
}
</style>