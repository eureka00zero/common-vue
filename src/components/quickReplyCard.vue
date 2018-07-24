<template>
  <div class="post_return_row no_line" @click="doReply">
    <div class="post_return_row_l">
      <figure class="post_return_row_img mini my">
        <img :src="quickInfo.userImg" class="img_width i_bg"> 
        <i class="post_return_row_ic"></i>
      </figure>
    </div> 
    <aside class="post_return_row_r">
      <input type="text" placeholder="我的回复…" readonly class="post_return_row_ipt">
    </aside>
  </div>
</template>
<script>
const defaultImg =
  "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABAQMAAAAl21bKAAAAA1BMVEUAAACnej3aAAAAAXRSTlMAQObYZgAAAApJREFUCNdjYAAAAAIAAeIhvDMAAAAASUVORK5CYII=";
// TODO: +V 信息  ic_v_blue ic_v_yellow
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
    // console.log("quick card created", this.data);
  },
  computed: {
    quickInfo: function() {
      let temp = Object.assign({}, this.data);
      temp.userImg = temp.__loginUserImg || defaultImg;
      return temp;
    }
  },
  methods: {
    doReply() {
      this.$emit("do-reply", { data: this.data });
    }
  }
};
</script>
