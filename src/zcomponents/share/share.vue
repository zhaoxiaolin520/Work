<template>
<div class="disk_item">
    <div class="disk_header">
        <div class="disk_header_title">
            <a href="javascript:;">
                <font-awesome-icon icon="folder" class="title_link" />
                <span>与我共享</span>
                <font-awesome-icon icon="angle-down" class="" />
            </a>
        </div>
    </div>
    <div class="disk_table">
      <empty></empty>
    </div>
</div>
</template>

<script>
import empty from "../empty/empty.vue";
export default {
  components:{
    empty
  }
};
</script>

<style lang="scss">
$colorGreen: rgb(34, 215, 187);
.disk_item{
  width: 100%;
}
.disk_header {
  display: flex;
  padding: 12px 17px;
  margin: 0;
  position: relative;
  background: rgba(253, 253, 253, 0.95);
  align-content: center;
  justify-content: space-between;
  .disk_header_title {
    a {
      font-size: 14px;
      .title_link {
        font-size: 19px;
        color: $colorGreen;
        margin-right: 8px;
      }
    }
  }
  .upload_file {
    .new_file {
      border: 1px solid $colorGreen;
      border-radius: 5px;
      padding: 3px 30px;
      font-size: 14px;
      color: $colorGreen;
      &:hover{
        background: $colorGreen;
        color:#fff;
      }
    }
  }
}
.disk_table {
  background: #fff;
  height: calc(100% - 80px);
  margin: 15px;
  order: 99;
  position: relative;
}
</style>
