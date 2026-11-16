# ARミニ太陽系（AR.js + A-Frame）

## 内容
- `index.html`：スマホでキツネのマーカーを読み取ると、太陽と6つの惑星が公転するAR作品。
- `preview.html`：マーカーを使わず、3Dをパソコンのブラウザで確認。
- `fox.patt`：授業で使ったキツネのマーカーの認識ファイル。
- `marker.png`：カメラで読み取るキツネのマーカー画像。
- `sun.jpg`, `mercury.jpg`, `venus.jpg`, `earth.jpg`, `mars.jpg`, `jupiter.jpg`, `saturn.jpg`：自作の惑星テクスチャ。

## GitHub Pagesでの公開
1. ZIPを展開。
2. リポジトリの一番上に `index.html` と `fox.patt` と7つの `.jpg` をアップロード。すべて同じ階層に置く。
3. すでに `index.html` があれば差し替え、既存の `fox.patt` はそのままでもよい。
4. `Settings > Pages` で `main`, `/(root)` を選ぶ（設定済みなら不要）。
5. `https://ユーザー名.github.io/リポジトリ名/?v=3` をスマホで開き、`marker.png` に向ける。

## 自作マーカーに変更するとき
授業資料の AR.js Marker Training で自作画像から `solar.patt` と印刷用画像を生成する。
`solar.patt` をアップロードして `index.html` の `<a-marker type="pattern" url="fox.patt" ...>` にある `url="fox.patt"` を `url="solar.patt"` に変更。

## 仕組み
- `a-sphere` に自作テクスチャ画像を貼り、惑星表面の色や模様を再現。
- `a-entity` を Y軸方向に回転させて、それぞれの惑星の公転を再現。
- `a-torus` で惑星と同じ高さに公転軌道を表示、`a-ring` で土星の輪を再現。
- `a-light` で光源を追加。

※惑星の距離、サイズ、公転周期は演出用で、実際の太陽系の比率ではありません。
※惑星の表面画像はこの制作セット用に生成したオリジナル画像です。インターネット由来の画像ではありません。

※ 太陽と6惑星の公転速度は作品用の演出です。惑星が表示されない場合はブラウザのカメラ使用許可、画像のアップロード場所、ファイル名を確認してください。
