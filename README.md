# 成都马拉松全马 · 2026-10-25

从金沙遗址博物馆出发，跑向成都世纪城新国际会展中心。路线使用 **2026-10-25 Joker 本人实际运动轨迹**，由 Apple 健康经 JPB 同步，共 13,290 个连续 WGS84 GPS 点，保留原始高程，标出人民南路折返、双林路折返、新九眼桥、环球中心与华阳大道折返。

[打开 3D 路线地图](https://joker-outdoor.github.io/chengdu-marathon-2026-10-25/) · [下载 GPX](data/route.gpx) · [打开 2D 俯视图](https://joker-outdoor.github.io/chengdu-marathon-2026-10-25/?view=2d)

页面提供真实卫星底图、3D 地形、2D 俯视、地标交互、联动海拔剖面与手机布局，并支持城市建筑开关、独立可调的建筑高度、沿线飞行的进度与倍速控制，以及按需加载的高清近景地表。飞行在折返和急弯处减速，以渐变转向舒缓镜头；沿线显示 1–42 公里标记。

## 距离与运动统计口径

- **手表运动距离 43.66 km**（原值 43.66188970686067 km）：来自 Apple 健康运动汇总，用于运动距离与平均配速计算。
- **GPS 几何长度 42.53 km**（原值 42.530570959229756 km）：按实际 WGS84 点逐段测距，保留全部轨迹点，不为对齐手表或官方距离而缩放坐标。
- **官方全马距离 42.195 km**：公里牌按官方赛程与 GPS 几何长度等比例定位；第 k 公里对应几何累计距离 k ÷ 42.195 × 42.530570959229756 km。飞行读数、地标里程与海拔剖面横轴使用这一口径，公里牌不是实测赛道牌位置。

运动汇总累计爬升 **110.53 m**，累计下降未提供。总耗时取运动结束时间减开始时间，为 **3h 43m 29.87s**（3.7249637302425174 小时）；暂停秒数取总耗时减运动时长的非负值，本次微小浮点误差归零，得到 0 秒。平均配速按手表距离及总耗时减暂停计算，约 5′07″/km。

海拔剖面直接使用轨迹原始高程（约 460.80–496.14 m），不以 DEM 采样替换，也不从高程起伏重算汇总爬升。DEM 只用于地图地形。公开 GPX 只包含路线名称、坐标和高程，不包含时间、设备信息或活动标识；原始 GPX 与运动汇总不入库。

## 地标定位

先从原复原路线的五个地标点提取 WGS84 经纬度，再匹配实际 GPS；三个折返沿原道路方向检查去返两侧，选择实际转向顶点。以下索引为实际轨迹的零起始索引，发生顺序已核验，不沿用旧索引。

| 地标 | 基线经度、纬度 | 实际轨迹索引 | 与基线位置距离 |
| --- | --- | ---: | ---: |
| 人民南路折返 | 104.0635723, 30.6545497 | 2661 | 约 179 m |
| 双林路折返 | 104.1082362, 30.6551343 | 4574 | 约 49 m |
| 新九眼桥 | 104.0873141, 30.6294170 | 6201 | 约 12 m |
| 环球中心 | 104.0660713, 30.5734993 | 8668 | 约 128 m |
| 华阳大道折返 | 104.0682845, 30.5065501 | 10971 | 约 57 m |

`route.config.json` 保存选定实际点的经纬度，由构建器匹配生成索引。人民南路实际折返比基线位置向南约 179 米；环球中心标记取实际经过的道路点。

## 资料与数据来源

- 实际轨迹和运动统计：Apple 健康经 JPB 同步的 Joker 本人 2026-10-25 运动记录；制作日期与运动日期均为 2026-10-25。
- [成都马拉松官方资料](https://chengdumarathon.cn/column/articleDetail/130?column_id=68&lang=cn)：赛程距离及起终点名称；地图中的路线坐标来自本人实际 GPS。
- [OpenStreetMap](https://www.openstreetmap.org/) 建筑轮廓及部件（parts）：复用 2026-10-24 围绕**原复原路线 500 米走廊**采集的 8,362 项绝对经纬度几何，未按新路线重新采集。逐点检查新轨迹到原路线线段的距离，最大约 251.32 米，全部 13,290 点处于原采集走廊且落在建筑数据地理外包范围内；这不表示新路线两侧完整 500 米均有建筑数据。© OpenStreetMap contributors，遵循 [ODbL](https://www.openstreetmap.org/copyright)。
- 建筑优先使用 OSM 标注高度，其中 OSM 自身标为估值的高度保留估值标记；只有楼层数时按每层 3 米估值，缺少高度时使用 12 米默认估值，数据中保留高度来源。建筑显示为浅灰体块，没有真实外墙贴图；电视塔使用部件与离地高度（minHeight）呈现，建筑高度夸张独立于地形高度。
- 卫星底图：[Esri World Imagery](https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer)，按新轨迹 bounds 重建 zoom 13 全景；近景采用 zoom 17 本地 JPEG 分块，成都纬度下原生地面分辨率约 1.03 米/像素。Imagery © Esri, Maxar, Earthstar Geographics, and the GIS User Community。
- DEM：[Tilezen / Mapzen Terrain Tiles](https://github.com/tilezen/joerd)，Terrarium zoom 12，按新轨迹同一 bounds 重新双线性采样，单位为米；SRTM / GMTED2010 courtesy of USGS，见[数据署名与许可](https://github.com/tilezen/joerd/blob/master/docs/attribution.md)。

## 本地数据构建

现有 `scripts/build_data.py` 已从私有输入重建 `data/route.json`、隐私最小化的 `route.gpx`、`terrain.json` 与 `satellite.jpg`，并复用 `buildings.json`。影像源使用本机已有真实瓦片缓存；DEM、全景与高清清单均依据新轨迹同一 bounds 计算。原始输入始终位于仓库外。

已使用真实源瓦片完整重建沿线 **87 块** zoom 17 本地 JPEG 及其清单；影像按实际轨迹选块，按地图 bounds 裁切并保留原生分辨率。近景按需加载，未加载区域显示 zoom 13 全景。

共享 `app.js`、脚本和样式未改动；测试未发现固定旧 632 点的断言。`buildings.json` 的几何与来源保持原样。建筑数据校验不代表逐建筑视觉核对。

## 模板版本

复用 [Joker Outdoor 路线可视化模板](https://github.com/joker-outdoor/route-visualization-template)，版本 [`35c05aecfedbebe35dcb76ac323a5ad03a576281`](https://github.com/joker-outdoor/route-visualization-template/commit/35c05aecfedbebe35dcb76ac323a5ad03a576281)。保留模板的生成器、页面交互、样式与依赖；数据处理实现与规则以该模板为唯一来源，本仓库仅同步使用，不另行维护一套核心实现。Three.js 0.160.0 使用 MIT 许可，见 `vendor/LICENSE`。
