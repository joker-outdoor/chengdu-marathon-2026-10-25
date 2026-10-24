# 成都马拉松全马 · 2026-10-25

从金沙遗址博物馆出发，跑向成都世纪城新国际会展中心。路线依据官方路线图与交警公布的道路顺序，结合 OpenStreetMap 道路坐标复原，共 632 个连续 WGS84 轨迹点，标出人民南路折返、双林路折返、新九眼桥、环球中心与华阳大道折返。

[打开 3D 路线地图](https://joker-outdoor.github.io/chengdu-marathon-2026-10-25/) · [下载 GPX](data/route.gpx) · [打开 2D 俯视图](https://joker-outdoor.github.io/chengdu-marathon-2026-10-25/?view=2d)

页面提供真实卫星底图、3D 地形、2D 俯视、地标交互、联动海拔剖面与手机布局。

## 距离与轨迹口径

官方全马距离为 **42.195 km**；复原坐标测算距离约 **43.72 km**。页面主里程使用官方距离，轨迹定位与海拔剖面使用坐标测距；保留复原坐标，不拉伸坐标来凑官方距离。

GPX 只包含路线名称、坐标和海拔，没有时间、速度或成绩。海拔来自 DEM 采样；累计爬升、下降及用时未提供，不把地形采样起伏累计为运动成绩。

## 资料与数据来源

- [成都马拉松官方路线图](https://chengdumarathon.cn/column/articleDetail/130?column_id=68&lang=cn)：路线走向、起终点与折返位置。
- [交警公布的道路顺序](https://news.chengdu.cn/2026/1020/6ad75848dfb5a2495acae467.shtml)：道路衔接与通行顺序。
- [OpenStreetMap](https://www.openstreetmap.org/) 道路几何用于坐标复原与地标对照；© OpenStreetMap contributors，遵循 [ODbL](https://www.openstreetmap.org/copyright)。
- 卫星底图：[Esri World Imagery](https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer)，zoom 13；Imagery © Esri, Maxar, Earthstar Geographics, and the GIS User Community。
- DEM：[Tilezen / Mapzen Terrain Tiles](https://github.com/tilezen/joerd)，Terrarium zoom 12，双线性采样，单位为米；SRTM / GMTED2010 courtesy of USGS，见[数据署名与许可](https://github.com/tilezen/joerd/blob/master/docs/attribution.md)。

## 模板版本

复用 [Joker Outdoor 路线可视化模板](https://github.com/joker-outdoor/route-visualization-template)，版本 [`acc8f4107cf933c03480c1570e0384a89276e99c`](https://github.com/joker-outdoor/route-visualization-template/commit/acc8f4107cf933c03480c1570e0384a89276e99c)。保留模板的生成器、页面交互、样式与依赖；Three.js 0.160.0 使用 MIT 许可，见 `vendor/LICENSE`。

本仓库使用已准备好的四份 `data/` 文件与根目录 `route.config.json`；原始输入、OSM 全量资料及官方 JPG 不纳入发布内容。
