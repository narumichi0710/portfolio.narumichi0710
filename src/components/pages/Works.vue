<template>
  <div id="works">
    <pageTitle title="Works"></pageTitle>
    <ul>
      <li>
        <a href="http://shairechat.com/" target="_blank">
        <img src="../../assets/Screen Shot 0002-10-20 at 19.51.33.png">
          <div class="content">
            <h3>ShaireChat (美容業従事者の方向けのフリマサイト)</h3>
            <p class="detail">美容室のフリマサイトです。
                使わなくなった物を他の美容室の誰かにあげたり、探している物を無料でもらえたり出来ます。
                レスポンシブ対応しているのでスマホからもご確認いただけます。
            </p>
            <p>PHP, Laravel, Vue.js, AWS</p>
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
import pageTitle from '../modules/pageTitle'

export default {
  components: {
    pageTitle,
  },
}
</script>

<style scoped>

#works {
  margin-top: -50px; /* 固定ナビの高さ分のネガティブマージン */
  padding-top: 100px; /* 打ち消し用のパディング */
  margin-bottom: 200px;
}

ul {
  display: flex;
  justify-content: space-evenly;
  padding-left: 0;
  width: 60%;
  margin: 0 auto;
}

li {
  list-style: none;
  text-align: center;
  border-radius: 5px;
  margin: 0 20px;
  transform-style: flat;
  transition: all 250ms ease-out;
  box-shadow: 0 2px 5px #ccc;
}

a {
  text-decoration: none;
}

p {
  color: rgb(50, 50, 50);
}

img {
  width: 100%;
  border-bottom: solid 1px #ccc;
}

.content {
  padding: 0 20px 20px;
}

.detail {
  text-align: left;
}

li:hover {
  box-shadow: 0 10px 15px rgba(31, 31, 31, 0.5);
}

@media screen and (max-width: 480px) {

  #works {
    margin-bottom: 100px;
  }

  ul {
    display: initial;
    width: 60%;
  }

  li {
    margin-bottom: 50px;
  }

  p {
    font-size: 15px;
  }
}

</style>
