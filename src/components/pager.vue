<template>
  <div class="pager-container">
    <a :class="{disabled: current === 1}" href="">|&lt;&lt;</a>
    <a :class="{disabled: current === 1}" href="">&lt;&lt;</a>
    <a href="">1</a><a href="">2</a><a href="">3</a><a href="">4</a><a href="">5</a><a href="">6</a><a href="">7</a><a href="">8</a><a href="">9</a><a href="">10</a>
    <a :class="{disabled: current === 1}" href="">&gt;&gt;</a>
    <a :class="{disabled: current === 1}" href="">&lt;&lt;|</a>
  </div>
</template>

<script>
export default {
  props:{
    current:{
      type:Number,
      default:1
    },
    total:{
      type:Number,
      default:0
    },
    limit:{
      type:Number,
      default:10
    },
    visibleNumber:{
      type:Number,
      default:10
    }
  },
  computed:{
    pageNumber(){
      return Math.ceil(this.total/this.limit);
    }
  }
}
</script>

<style lang="less" scoped>
@import '~@/styles/var.less';
  .pager-container{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: @re;
    a{
      margin: 0 7px;
      &.disabled{
        color:gray;
        cursor: not-allowed;
      }
    }
  }

</style>