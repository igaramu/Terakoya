<template>
  <div id="home">
    <Header/>
    <div class="body">
      <Sidebar/>
      <div class="content">
        <div v-html="$md.render(docs)"></div>
      </div> <!--/top-content-->
    </div> <!--/body-->
  </div> <!--/home-->
</template>

<script lang="ts">
import Vue from 'vue';

import Docs from '/src/main/docs.md';
import Header from '/components/Header.vue';
import Sidebar from '/components/SideBar.vue';

export default Vue.extend({
  components: {Header, Sidebar},
  data() {
    return {
      docs: Docs,
    }
  },
})

</script>

<style lang="scss">
@import "style/style";
</style>
