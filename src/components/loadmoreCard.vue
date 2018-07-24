<template>
  <div class="post_return_row" :class="{'more_list': data.__singleLoadmore}">
    <div class="post_return_row_l"></div> 
    <aside class="post_return_row_r">
      <a href="javascript:void(0)" class="post_return_more" :class="{'hide': data.__showLoading}" style="text-indent:initial" @click="doSecLoadmore">查看剩余<span>{{data.__remainCount}}</span>条{{showCMNTName}}...</a >
      <a :class="{'hide': !data.__showLoading}"  class="cm_loading"><img class="img_width" src="../img/loading.gif" />加载中...</a>
    </aside>
  </div>
</template>
<script>
export default {
  props: {
    data: {
      type: Object,
      required: true
    },
    config:{
      type: Object
    }
  },
  created() {
    // console.log("create");
    this.showCMNTName = this.config.showName || '评论'
  },
  methods: {
    doSecLoadmore() {
      this.$emit("do-sec-loadmore", { data: this.data });
    }
  }
};
</script>
