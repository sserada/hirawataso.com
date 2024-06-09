<template>
  <v-container>
    <v-infinite-scroll :height="600" side="none">
      <v-row>
        <v-col cols="12" sm="4" md="4" lg="4">
          <v-card class="card">
            <v-card-item>
              <v-card-title class="title-en">Portfolio Site</v-card-title>
            </v-card-item>
            <v-card-text class="text">
              私のポートフォリオ兼ブログサイトです．<br />
              主にVue 3 + anime.jsで開発されています．<br />
            </v-card-text>
            <a class="url" target="_blank" href="https://github.com/fightingso/portfolio">GitHub</a>
          </v-card>
        </v-col>

        <v-col cols="12" sm="4" md="4" lg="4">
          <v-card class="card">
            <v-card-item>
              <v-card-title class="title-en">Server Monitor</v-card-title>
            </v-card-item>
            <v-card-text class="text">
              サーバ監視用のDiscord Botです．<br />
              Discord.pyで開発されており，メモリとVRAMの使用量，ログインユーザの確認ができるようになっています．<br />
            </v-card-text>
            <a class="url" target="_blank" href="https://github.com/fightingso/server-monitor">GitHub</a>
          </v-card>
        </v-col>

        <v-col cols="12" sm="4" md="4" lg="4">
          <v-card class="card">
            <v-card-item>
              <v-card-title class="title-en">Neuro Composer</v-card-title>
            </v-card-item>
            <v-card-text class="text">
              ユーザの創造性を支援する対話型自動作曲システムです．<br />
              フロントエンドはSvelteで開発されており，バックエンドとWebSocket通信が行われます．<br />
              バックエンドは主にFastAPI + Tensorflowで開発されており，LSTMで楽曲を生成し，楽曲に対するユーザ評価を元に粒子群最適化によるモデルのパラメータ調整が行われます．
            </v-card-text>
            <a class="url" target="_blank" href="https://arxiv.org/abs/2403.03395">arXiv</a>
          </v-card>
        </v-col>

        <v-col cols="12" sm="4" md="4" lg="4">
          <v-card class="card">
            <v-card-item>
              <v-card-title class="title-en">WebSocket Sample</v-card-title>
            </v-card-item>
            <v-card-text class="text">
              WebSocketで画像を送受信するサンプルです．<br />
              フロントエンドはSvelte, バックエンドはFastAPIで開発されており，フロントエンドでアップロードした画像がバックエンドで白黒に変換され返されるようになっています．<br />
              また，画像は分割送受信され高画質画像にも対応しています．
            </v-card-text>
            <a class="url" target="_blank" href="https://github.com/fightingso/websocket-sample">GitHub</a>
          </v-card>
        </v-col>

        <v-col cols="12" sm="4" md="4" lg="4">
          <v-card class="card">
            <v-card-item>
              <v-card-title class="title-en">Ok Yoshida</v-card-title>
            </v-card-item>
            <v-card-text class="text">
              観葉植物の水やりを管理するLINE Botです．<br />
              GASで開発されており，水やりを記録し，最後に水をあげた日にちを確認できるようになっています．
            </v-card-text>
            <a class="url" target="_blank" href="https://github.com/fightingso/ok-yoshida">GitHub</a>
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

