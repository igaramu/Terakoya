<template>
  <div id="home">

    <section class="top">
      <Header/>
      <div class="top-content">
        <h1>IgaraSystem</h1>
        <p>プログラミングが１からわかる</p>
        <p>初学者向け無料マニュアル</p>
        <b-button type="is-primary is-light">はじめる</b-button>
        <b-button>IgaraSystemとは？</b-button>
<!--        <div v-html="$md.render(model)">aaa</div>-->
      </div> <!--/top-content-->
    </section>

    <section class="main">

      <h2>初学者を徹底サポート！</h2>
      <div class="main-content">
        <div class="left-img">
          <img src="~/src/pose_zasetsu.png">
        </div>
        <article>
          <div class="message">
            <p>何から始めたら良いのかわからない</p>
            <p>実践にどうやって活かしたらよいのか</p>
            <p>よくわからなくなって辞めてしまった…</p>
          </div>
        </article>
      </div>

      <h2>丁寧なマニュアル</h2>
      <div class="sub-content">
        <article>
          <div class="message">
            <p>テキストベースなので好きなときに見れる</p>
            <p>環境構築から説明</p>
            <p>エラーへの対応も充実</p>
          </div>
        </article>
        <div class="right-img">
          <img src="~/src/pc.png">
        </div>
      </div>

    </section> <!--/main-->


  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import VBA_1 from '/src/vba/vba_1.md';
import HTML_1 from '/src/vba/vba_2.md';
import Header from '/components/Header.vue';

export default Vue.extend({
  name: 'IndexPage',
  components: Header,
  data() {
    return {
      model: VBA_1,
      model2: HTML_1
    }
  }
})

</script>

<style lang="scss">
@import "style/style.scss";
</style>

