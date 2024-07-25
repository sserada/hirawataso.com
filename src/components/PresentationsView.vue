<template>
  <v-container>
    <v-infinite-scroll :height="600" side="none">
      <v-row>
        <v-col cols="12" sm="4" md="4" lg="4">
          <v-card class="card">
            <v-card-item>
              <v-card-title class="title-ja">内閣府 総合知ワークショップ</v-card-title>
              <v-card-subtitle class="title-ja">2024年6月6日</v-card-subtitle>
            </v-card-item>
            <v-card-text class="text">
              東京都市大学で開講される講義"SD PBL"が総合知滋養にどのように役立っているのか，学生の視点からお話ししました．<br />
            </v-card-text>
            <a class="url" target="_blank" href="https://www.tcu.ac.jp/news/all/20240628-58059/">News</a>
          </v-card>
        </v-col>

        <v-col cols="12" sm="4" md="4" lg="4">
          <v-card class="card">
            <v-card-item>
              <v-card-title class="title-en">the 16th International Symposium on Computer Music Multidisciplinary Research</v-card-title>
              <v-card-subtitle class="title-ja">2023年11月</v-card-subtitle>
            </v-card-item>
            <v-card-text class="text">
              ポスターセッションではプロのミュージシャンとコラボして，自動作曲システムで子守唄を作成した事例について，デモセッションではコーヒを抽出する際の楽曲を生成する自動作曲システムに関する研究発表を行いました．
            </v-card-text>
          </v-card>
        </v-col>

        <v-col cols="12" sm="4" md="4" lg="4">
          <v-card class="card">
            <v-card-item>
              <v-card-title class="title-ja">GitHub講習会</v-card-title>
              <v-card-subtitle class="title-ja">2023年5月5日</v-card-subtitle>
            </v-card-item>
            <v-card-text class="text">
              後輩約50名に対して，GitHubの基本的な仕組み，使い方を教える講習を行いました．
            </v-card-text>
            <a class="url" target="_blank" href="https://speakerdeck.com/fightingsou/githubjiang-xi-hui-2023">Slide</a>
          </v-card>
        </v-col>

        <v-col cols="12" sm="4" md="4" lg="4">
          <v-card class="card">
            <v-card-item>
              <v-card-title class="title-en">TCU R-PresCo</v-card-title>
              <v-card-subtitle class="title-ja">2022年11月5日</v-card-subtitle>
            </v-card-item>
            <v-card-text class="text">
              共生進化アルゴリズムを用いたモザイクアート生成に関する研究発表を行い，優秀賞を獲得しました．
            </v-card-text>
            <a class="url" target="_blank" href="https://informatics.tcu.ac.jp/news/award/?&p=841">News</a>
          </v-card>
        </v-col>

      </v-row>
    </v-infinite-scroll>
  </v-container>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@200..900&display=swap');

  .card {
    padding: 15px;
  }

  .card:hover {
    transform: translateY(-5px);
    transition: 0.3s;
  }

  .title-ja {
    font-family: "Noto Serif JP", serif;
    opacity: 0.8;
  }

  .title-en {
    font-family: 'Great Vibes', cursive;
    opacity: 0.8;
  }

  .text {
    font-family: "Noto Serif JP", serif;
    opacity: 0.8;
  }

  .url {
    font-family: "Noto Serif JP", serif;
    font-size: 14px;
    opacity: 0.8;
    color: #ff6347;
    text-decoration: none;
  }

  .url:hover {
    color: #eee;
    transition: 0.3s;
  }
</style>

