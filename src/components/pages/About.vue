<template>
  <div id="about">
    <pageTitle title="About me"></pageTitle>
    <div class="items">
      <div class="portfolio-images">
        <div class="my-img">
          <img src="../../assets/IMG_7157.jpeg">
        </div>
        <ul class="sns-images">
          <li><a href="https://www.facebook.com/profile.php?id=100006111796806" target="_blank"><img src="../../assets/icon-facebook.svg" class="sns"></a></li>
          <li><a href="https://www.instagram.com/naruhairdesigns" target="_blank"><img src="../../assets/icon-instagram.jpeg" class="sns"></a></li>
           <li><a href="https://twitter.com/naruhairdesigns" target="_blank"><img src="../../assets/icon-twitter.svg" class="sns"></a></li>
          <li><a href="https://github.com/narumichi0710" target="_blank"><img src="../../assets/icon-github.png" class="sns"></a></li>
        </ul>
      </div>
      <ul class="content">
        <li>
          <h3>Name</h3>
          <p>Narumichi Kubo</p>
          <h3>Age</h3>
          <p>23</p>
          <h3>Birthplace</h3>
          <p>Osaka, Japan</p>
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
  }
}
</script>
<style scoped>

#about {
  margin-top: -50px; /* 固定ナビの高さ分のネガティブマージン */
  padding-top: 100px; /* 打ち消し用のパディング */
}

.items {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  width: 50%;
  margin: 0 auto 100px;
  color: rgb(50, 50, 50);
}

.my-img {
  display: flex;
  align-items: center;
  justify-content: center;
}

.my-img img {
  width: 70%;
  border-radius: 100%;
}

.sns-images {
  display: flex;
  justify-content: center;
  margin-top: 50px;
  padding-left: 0;
}

li {
  list-style: none;
}

.sns {
  width: 30px;
  margin: 0 15px;
  filter: grayscale(100%);
}

.sns:hover {
  filter: grayscale(0);
}

.content {
  width: 80%;
  padding-left: 0;

}

.content li {
  margin-bottom: 20px;
}

.content h3, .content p {
  margin: 10px;
}

.content p {
  white-space: pre-wrap
}

@media screen and (max-width: 480px) {

  .items {
    display: initial;
  }

  .portfolio-images {
    margin-bottom: 50px;
  }
  .my-img img {
    width:50%;
  }

  .sns-image{
    font-size:10px;
  }

  .content {
    width: 100%;
    text-align:center;
  }

  .content h3 {
    font-size: 20px;
  }

  .content p {
    font-size: 15px;
  }
}

</style>
