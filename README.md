# FLAVOR STRUCTURE LAB β — 味覚構造体ジェネレーター

味覚を、自由な質量・骨格・表面・色彩の関係として生成するブラウザ用3Dアプリの試作版です。

## アプリを開く

**GitHub Pages:** https://furuinu.github.io/-flavor-structure-lab/

> GitHub Pages が有効になり、デプロイが成功した後に利用できます。アプリ本体は単一ファイル `index.html` です。ローカルのブラウザでも動作します。

## 操作

1. `完全ランダム生成` を押すと、新しいシードから独立した左右の造形を作ります。
2. 画面をドラッグして回転、ピンチ/ホイールで拡大縮小します。
3. 左右の融合や造形パラメータを調整できます。
4. 同じシードと同じ設定なら再現可能です。PNG・設定JSONを保存できます。

## カラーパレット

元の **6列×81行** のパレットを使用します。毎回異なる2行を選択し、それぞれから異なる3列の色を選んで左右の構造体に割り当てます（計6サンプル）。`palette.json` は参照用で、アプリにもデータを内蔵しています。

## 3D実装

左右独立した造形アルゴリズム、SDFの加算・減算、メッシュ化、骨格、7種類の中央接合関係、シード管理、WebGL/Canvas表示を実装した試作版です。GLB出力、高度な一体ブーリアン、レンダリング品質向上は今後の開発対象です。表示や造形は端末・ブラウザの性能によって変わる場合があります。

## 初回の無料公開設定

1. [Settings → Pages](https://github.com/furuinu/-flavor-structure-lab/settings/pages) を開く。
2. `Build and deployment` の `Source` で **GitHub Actions** を選ぶ。
3. [Actions → Deploy Flavor Structure Lab](https://github.com/furuinu/-flavor-structure-lab/actions/workflows/deploy.yml) で `Run workflow` → `main` → `Run workflow`。
4. 緑色の完了後、上記の GitHub Pages URL にアクセスする。反映には数分かかることがあります。

このリポジトリは **Public** です。GitHub Freeの公開リポジトリならGitHub Pagesを無料で利用できます。公開サイトのソースコードも閲覧可能です。以前の非公開の `masala-generator` は公開・変更していません。
