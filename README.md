# OSM Assessment

## 概要
以下の論文で使用しているOSM道路データとDRMデータの比較結果です  
- 金杉洋, 瀬戸寿一，関本義秀，柴崎亮介, **オープンストリートマップ道路データとデジタル道路地図の比較　- 位置と完全性に着目して -** , GIS-理論と応用, Vol.27, No.1, pp.43-48, 2019.06

## データファイル
- *27-1-43-GISA-paper.pdf*: 論文本体
- *motorway_accuracy_mesh.tsv* : 位置精度比較結果
	- meshcode: 三次メッシュコード(1km メッシュ)
	- osm_length: 当該メッシュにおけるOSM motorway 延長(m)
	- overlap_length: DRM道路幅員バッファと交差するOSM motorwayの延長(m)
	- overlap_length_max: 位置標準誤差を含むDRM道路幅員バッファと交差するOSM motorwayの延長(m)
	- accuracy: OSM motorwayの位置精度 [overlap_length / osm_length]
	- accuracy_max: OSM motorwayの位置精度(DRM位置標準誤差を含む) [overlap_length_max / osm_length_max]
- *coverage_city.tsv* : 市区町村別網羅率
	- city_code: 市区町村コード
	- pref_name: 都道府県名
	- district_name: 支庁名
	- city_name: 郡・政令都市名
	- name: 都市名
	- drm_length: 当該市区町村におけるDRM道路延長(m)
	- osm_length: 当該市区町村におけるOSM道路延長(m)
	- completeness: 完全性（道路延長差分(m) [osm_length - drm-lenth]）
	- coverage: 網羅率（道路延長比(m) [osm_length / drm-lenth]) 
- *coverage_mesh.tsv* : メッシュ別網羅率
	- meshcode: 三次メッシュコード(1km メッシュ)
	- drm_length: 当該メッシュにおけるDRM道路延長(m)
	- osm_length: 当該メッシュにおけるOSM道路延長(m)
	- completeness: 完全性（道路延長差分(m) [osm_length - drm-lenth]）
	- coverage: 網羅率（道路延長比(m) [osm_length / drm-lenth]) 

## 元データ
- OpenStreetMap: [Geofabric](http://download.geofabrik.de/asia/japan.html)より取得した2017年7月26日時点のデータを使用しています
- デジタル道路地図(DRM): 東京大学空間情報科学研究センターの共同利用データで提供されている，[拡張版全国デジタル道路地図データベース2017年版](https://joras.csis.u-tokyo.ac.jp/dataset/show/id/900014201700)を使用しています
- 行政区域: [国土数値情報行政区域 平成29年](http://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-N03-v2_3.html)

## 注意
- 本データは論文の分析結果の参考としてデータ公開するものです．引用等される場合は出典を明示してください

