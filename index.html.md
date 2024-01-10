ホスティング事業部 SREチームの [@takumakume](https://twitter.com/takumakume) です。

11/21に「[技術的負債に向き合う Online Conference](https://findy.connpass.com/event/297813/)」 が開催されました。
ペパボからは、技術責任者の [@kenchan](https://twitter.com/kenchan) と @takumakume が登壇しました。

この記事では、@takumakume が登壇した「ソフトウェアの継続的アップデートをコンテナ化によって加速させる」というタイトルのLTについて紹介します。LTでは駆け足の説明でしたので、補足的な位置づけとなります。

<script defer class="speakerdeck-embed" data-id="f49f05833a0c46b3b2b1e58fbb3f3419" data-ratio="1.7772511848341233" src="//speakerdeck.com/assets/embed.js"></script>

簡単に説明すると

**変更しにくいシステムは放置されるので、コンテナ化して変更しやすくした！**

という話です。

以降で詳しく説明していきます。

## ソフトウェアアップデートの必要性について

![ソフトウェアをアップデートしなかったらどうなるか](2.jpg)

![継続的にソフトウェアアップデートをしなかったらどうなるか](3.jpg)

ソフトウェアを継続的にアップデートしなければシステムは徐々に壊れていきます。予想外のタイミングと規模でアップデートを強制されることに繋がり、ビジネスに悪影響を及ぼします。

例えば「Ruby on rails のバージョンを上げたいが、 MySQL のバージョンも上げる必要がある。」「OpenSSLのバージョンを上げたいがパッケージが提供されていないため、OSを上げるか自前でビルドするか選択する」といったケースです。

...

