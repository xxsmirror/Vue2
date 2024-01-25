<template>
  <div id="app">
    <Avatar url="https://i8.meishichina.com/attachment/recipe/2012/10/23/20121023114134207352734.jpg@!p800" :height="500" :weight="200"/>
    <Icon type="1"></Icon>
    <Pager></Pager>
  </div>
</template>

<script>
import Avatar from './components/Avatar.vue';
import Icon from './components/Icon.vue';
import Pager from './components/pager.vue';

export default {
  components: {
    Avatar,
    Icon,
    Pager
  }
}
</script>


