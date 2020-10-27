<template>
  <div id="skills">
    <pageTitle title="Skills"></pageTitle>
    <div class="items">
      <p class="sub-title"></p>
      <ul>
        <li v-for="(language, index) in languages" :key="index" v-on:mouseover="mouseOverAction(index)" v-on:mouseleave="mouseLeaveAction(index)">
          <img v-bind:src="language.url">
          <h5>{{ language.name }}</h5>
          <p v-if="isHover && isIndex === index" class="detail">{{ language.detail }}</p>
        </li>
      </ul>
    </div>
  </div>
</template>


<script>
import pageTitle from '../modules/pageTitle'
export default {
  components: {
    pageTitle,
  },
  data() {
    return {
      isHover: false,
      isIndex: '',
      languages: [
        { url: 'https://cdn.svgporn.com/logos/html-5.svg', name: 'HTML', detail: 'セマンティクスとツリー構造を意識した基本的なレイアウトが書けます。' },
        { url: 'https://cdn.svgporn.com/logos/css-3.svg', name: 'CSS', detail: '基本的なデザインが書けます。\nレスポンシブ可。' },
        { url: 'https://cdn.svgporn.com/logos/javascript.svg', name: 'javascript', detail: 'プログラミングスクールで勉強した言語です。\nTypeScriptも勉強しており、何か制作物を作りたいです。'},
        { url: 'https://cdn.svgporn.com/logos/vue.svg', name: 'Vue.js', detail: 'このポートフォリオサイトを開発するために勉強しました。' },
        { url: 'https://cdn.svgporn.com/logos/php.svg', name: 'PHP', detail: '今のところ最も触っている言語です。就活用のポートフォリオはPHPで勉強しました。' },
        { url: 'https://cdn.svgporn.com/logos/laravel.svg', name: 'laravel', detail: '今のところ最も触っているフレームワークです。\n就活用のポートフォリオはLaravelで勉強しました。' },
        { url: 'https://cdn.svgporn.com/logos/docker-icon.svg', name: 'Docker', detail: ''},
        { url: 'https://cdn.svgporn.com/logos/aws.svg', name: 'AWS', detail: '基本的なシステム構成を理解しており、就活用のポートフォリオを開発する際に勉強しました。'},
        ]
    }
  },
  methods: {
    mouseOverAction(index) {
      this.isHover = true;
      this.isIndex = index;
    },
    mouseLeaveAction() {
      this.isHover = false;
    },
  }
}
</script>



<style scoped>

#skills {
  margin-top: -50px; /* 固定ナビの高さ分のネガティブマージン */
  padding-top: 100px; /* 打ち消し用のパディング */
  margin-bottom: 100px;
}

.items {
  width: 70%;
  margin: 0 auto;
  color: rgb(50, 50, 50);
}

.sub-title {
  text-align: center;
  margin-bottom: 50px;
}

img {
  height: 50px;
}

ul {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  align-items: top;
  padding-left: 0;
}

li {
  list-style: none;
  text-align: center;
  width: 25%;
  padding-top: 10px;
  /* padding: 20px; */
  filter: grayscale(100%);
}

li:hover {
  cursor: pointer;
  /* box-shadow: 0 2px 5px #ccc; */
  filter: grayscale(0);
}

.detail {
  /* text-align: left; */
  font-size: 14px;
}

p {
  white-space: pre-wrap
}

@media screen and (max-width: 480px) {
  #skills {
    margin-bottom: 0;
  }

  li {
    text-align: center;
    width: 50%;
    padding-top: 10px;
    /* padding: 20px; */
    filter: grayscale(100%);
  }

  .detail {
    font-size: 15px;
  }

  p {
    font-size: 15px;
  }
}

</style>
