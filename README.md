# freebusmap
自由なバスマップをみんなの手に

freebusmap（フリーバスマップ）は誰でも自由にバスマップを作って、使えるプロジェクトです。
現在のバスだけでなく、過去のバスや架空バス、鉄道や航路、その他なんでも大丈夫です。
freebusmapはバスマップ自動描画システムbusmapjsを使います。
busmapjsがあらゆるバスマップに共通する描画システムであるのに対し、freebusmapは個々のバスのデータを作るものです。
ライセンスはCC0 1.0とします。

## サンプル
現在は試験的に<a href="https://github.com/toyotamakenkyusyo/freebusmap/blob/master/test.geojson">https://github.com/toyotamakenkyusyo/freebusmap/blob/master/test.geojson</a>にデータがあります。  
<a href="https://toyotamakenkyusyo.github.io/freebusmap/freebusmap_test.xhtml">https://toyotamakenkyusyo.github.io/freebusmap/freebusmap_test.xhtml</a>でバスマップが表示されます。


## 参加方法
freebusmapはGitHubでデータを管理しています。このデータは誰でも自由に使うことができます。
データを作ったり、変えたい場合は、GitHubのプルリクエスト機能やissue機能をご利用ください。この方法はGitHubへの登録が必要になるため、この他メール等でご連絡いただくことも可能です。


## データの作り方
freebusmapのデータはGeoJSON形式と互換性のある独自形式を用いています。なお、busmapjsはGTFS等の他のデータ形式にも対応しています。  
データはバス停車位置、交差点、道路、運行系統の4つからなります。  
バス停車位置は概ね停留所標柱と対応しますが、同じ停車位置に複数本の標柱がある場合は1つにまとめます。  
交差点と道路は国土地理院ベクトルタイル道路中心線の緯度経度を使用します。交差点名がある場合はそれを用い、ない場合は重複しないように適切な名をつけます。  
道路のデータは<a href="https://ss1.xrea.com/toyotama.g1.xrea.com/bus/gtfsbusmap/rdclshapes/rdclshapes.xhtml">https://ss1.xrea.com/toyotama.g1.xrea.com/bus/gtfsbusmap/rdclshapes/rdclshapes.xhtml</a>等を用いて緯度経度を集めます。  
運行系統は通る停車位置と交差点名をそれぞれ配列としてもちます。
