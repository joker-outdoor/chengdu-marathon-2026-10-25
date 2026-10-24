# 成都马拉松全马 · 2026-10-25

从金沙遗址博物馆出发，跑向成都世纪城新国际会展中心。路线依据官方路线图与交警公布的道路顺序，结合 OpenStreetMap 道路坐标复原，共 632 个连续 WGS84 轨迹点，标出人民南路折返、双林路折返、新九眼桥、环球中心与华阳大道折返。

[打开 3D 路线地图](https://joker-outdoor.github.io/chengdu-marathon-2026-10-25/) · [下载 GPX](data/route.gpx) · [打开 2D 俯视图](https://joker-outdoor.github.io/chengdu-marathon-2026-10-25/?view=2d)

页面提供真实卫星底图、3D 地形、2D 俯视、地标交互、联动海拔剖面与手机布局，并支持城市建筑开关、独立可调的建筑高度、沿线飞行的进度与倍速控制，以及按需加载的高清近景地表。

## 距离与轨迹口径

官方全马距离为 **42.195 km**；复原坐标测算距离约 **43.72 km**。页面主里程使用官方距离，轨迹定位与海拔剖面使用坐标测距；保留复原坐标，不拉伸坐标来凑官方距离。

GPX 只包含路线名称、坐标和海拔，没有时间、速度或成绩。海拔来自 DEM 采样；累计爬升、下降及用时未提供，不把地形采样起伏累计为运动成绩。

## 资料与数据来源

- [成都马拉松官方路线图](https://chengdumarathon.cn/column/articleDetail/130?column_id=68&lang=cn)：路线走向、起终点与折返位置。
- [交警公布的道路顺序](https://news.chengdu.cn/2026/1020/6ad75848dfb5a2495acae467.shtml)：道路衔接与通行顺序。
- [OpenStreetMap](https://www.openstreetmap.org/) 道路几何用于坐标复原与地标对照；沿线 500 米范围内的 8,362 项建筑轮廓及部件（parts）也来自 OSM，提取日期为 2026-10-24；© OpenStreetMap contributors，遵循 [ODbL](https://www.openstreetmap.org/copyright)。
- 建筑优先使用 OSM 标注高度，其中 OSM 自身标为估值的高度保留估值标记；只有楼层数时按每层 3 米估值，缺少高度时使用 12 米默认估值，数据中保留高度来源。建筑显示为浅灰体块，没有真实外墙贴图；电视塔使用部件与离地高度（minHeight）呈现，建筑高度夸张独立于地形高度。
- 卫星底图：[Esri World Imagery](https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer)，保留 zoom 13 全景；近景使用已准备的 85 个 zoom 17 本地 JPEG 分块，成都纬度下原生地面分辨率约 1.03 米/像素，沿线按需加载。Imagery © Esri, Maxar, Earthstar Geographics, and the GIS User Community。
- DEM：[Tilezen / Mapzen Terrain Tiles](https://github.com/tilezen/joerd)，Terrarium zoom 12，双线性采样，单位为米；SRTM / GMTED2010 courtesy of USGS，见[数据署名与许可](https://github.com/tilezen/joerd/blob/master/docs/attribution.md)。

## 模板版本

复用 [Joker Outdoor 路线可视化模板](https://github.com/joker-outdoor/route-visualization-template)，版本 [`37ea8f97fbd75c4dc112fa4a21354111468fcfdf`](https://github.com/joker-outdoor/route-visualization-template/commit/37ea8f97fbd75c4dc112fa4a21354111468fcfdf)。保留模板的生成器、页面交互、样式与依赖；数据处理实现与规则以该模板为唯一来源，本仓库仅同步使用，不另行维护一套核心实现。Three.js 0.160.0 使用 MIT 许可，见 `vendor/LICENSE`。

本仓库使用已准备好的 `data/route.json`、`route.gpx`、`terrain.json`、`satellite.jpg`、`buildings.json`、`imagery-detail.json` 与 `imagery-detail/` 下的 85 个 JPEG 分块，以及根目录 `route.config.json`。路线点、统计与地标保持原样，route.json 仅新增建筑与近景影像文件引用；原始输入、OSM 全量资料及官方 JPG 不纳入发布内容。
