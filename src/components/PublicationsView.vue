<template>
  <div id="publications-container">
    <v-infinite-scroll :height="400" side="none">
      <ul>
        <li class="list-item" v-for="(publication, index) in publications" :key="index">
          <h3>{{ publication.title }}</h3>
          <p class="authors">{{ publication.authors }}</p>
          <p>{{ publication.journal }}</p>
        </li>
      </ul>
    </v-infinite-scroll>
  </div>
</template>

<script>
export default {
  data() {
    return {
      publications: [
        {
          title: 'StableDiffusionによる作家性が再現された画像の生成',
          authors: '若月玲之, 平綿素望, 大谷紀子',
          journal: '東京都市大学横浜キャンパス情報メディアジャーナル (25) 5-10 2024年3月',
        },
        {
          title: '生成AIを用いた質的研究法のデータ分析に関する検討',
          authors: '平綿素望, 大谷紀子, 岡部大介',
          journal: '東京都市大学横浜キャンパス情報メディアジャーナル (25) 11-19 2024年3月',
        },
        {
          title: 'Automatic Music Composition System to Enjoy Brewing Delicious Coffee',
          authors: 'Noriko Otani, So Hirawata, Daisuke Okabe',
          journal: 'Proceedings of the 16th International Symposium on Computer Music Multidisciplinary Research 736-739 2023年11月',
        },
        {
          title: 'Creating a New Lullaby Using an Automatic Music Composition System in Collaboration with a Musician',
          authors: 'So Hirawata, Noriko Otani, Daisuke Okabe, Masayuki Numao',
          journal: 'Proceedings of the 16th International Symposium on Computer Music Multidisciplinary Research 524-535 2023年11月',
        },
        {
          title: '進化計算を用いた画像配置の最適化によるモザイク写真生成',
          authors: '御手洗拓弥, 平綿素望, 大谷紀子',
          journal: '東京都市大学横浜キャンパス情報メディアジャーナル (24) 4-7 2023年3月',
        },
      ],
    };
  },
};
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@200..900&display=swap');

  #publications-container {
    max-width: 65%;
    margin: 0 auto;
    padding: 20px;
    border-radius: 8px;
    overflow-y: scroll;
    color: #f5f5f5;
  }

  .list-item {
    width: 100%;
    padding: 10px;
    text-align: left;
    margin-bottom: 10px;
    border-radius: 4px;
    border: #eee;
    transition: transform 0.3s ease-in-out;
  }

  .list-item:hover {
    transform: translateY(-5px);
  }

  h3 {
    font-family: "Noto Serif JP", serif;
    font-weight: 700;
    color: #f5f5f5;
    opacity: 0.8;
    margin-bottom: 5px;
  }

  p {
    font-family: "Noto Serif JP", serif;
    font-weight: 400;
    color: #ccc;
    margin: 0;
  }

  .authors {
    opacity: 0.7;
  }

  @media (max-width: 768px) {
    #publications-container {
      max-width: 100%;
    }

    h3 {
      font-weight: 400;
      font-size: 15px;
    }

    p {
      font-size: 12px;
    }
  }
</style>

