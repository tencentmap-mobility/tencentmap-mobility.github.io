# Android导航SDK Changelog

## v5.3.4 (2021-11-29)
1.	重构导航服务数据序列化反序列化模块。
2. 优化电子眼展示，支持最多3排展示。
3. 优化放大图预下载机制。
4. 优化伴随气泡展示位置。
5. 更新导航路线上的红绿灯图片资源，展示效果更佳。
6. 调整CarNaviView默认的最小比例尺，从14调整为15。

## v5.3.3 (2021-10-29)
1. CarNaviManager新增导航中修改算路策略方法(changeSearchOptions:);
2. CarRouteSearchOptions新增算路策略：是否大路优先(bigRoad)、是否优先时间短(shortTime)、是否优先高速(highway)；
3. GuidedLaneInfo新增numOfLane， 车道数；
4. CarRouteSearchOptions新增参数initialRouteID、initialNaviSessionID用于乘客选路功能。

## v5.3.2 (2021-09-27)
1. NaviPoi新增setSearchNaviPoiType()方法。开发者可选择起终点参数是否使用区域面反查POI策略;
2. CarNaviManager新增changeDestinationAndWays ()方法，导航过程可同时修改终点、途径点;
3. CarNaviView新增setEnlargedIntersectionAspectRatio()字段，路口放大图可修改宽高比;
4. 补齐限停摄像头;
5. NaviPoi算路起终点新增setPoiName()方法，允许开发者传入，该参数暂不影响算路策略;
6. 修复了开启多路线时，开启导航、偏航时导航卡顿的问题。

## v5.3.1 (2021-09-01)
1. 新增导航过程修改途径点接口;
2. 新增导航过程中修改目的地接口；
3. 路径规划返回红绿灯数据，导航地图展示路线上的红绿灯。


## v5.3.0.3 (2021-08-27)
1. 修复导航回调的定位点时间戳错误。

## v5.2.9.7 (2021-08-27)
1. 修复导航过程偶现少展示一张放大图的问题；
2. 修复开启导航前一分钟，偶现剩余时间不准的问题。

## v5.3.0.2 (2021-08-19)
1. 修复导航过程偶现少展示一张放大图的问题；
2. 修复开启导航前一分钟，偶现剩余时间不准的问题；
3. 修复导航过程中调用路径规划服务再发生偏航时，终点错误问题。

## v5.3.0.0 (2021-07-30)
1. 更新了导航引擎，提升整体导航体验
2. 支持arm64-v8a, armeabi-v7a, x86架构
3. 修复偶现的路况数据与路线点串数据对应不上的问题
4. 修复日夜间模式切换时回调不准的问题

## v5.2.9.6 (2021-07-15)
1. 优化自动比例尺缩放的路口增强策略；
2. CarNaviView新增setAutoScaleMinZoomLevel(…)方法，开发者可以设置导航过程中3D导航模式自动比例的最小zoomlevel值;
3. 修复路线上的路名无法删除的问题；
4. 修复CarNaviView剩余全览模式偶现crash

## v5.2.9.3 (2021-06-25)
1. 修复导航结束有线程未被销毁的情况

## v5.2.8.6 (2021-06-25)
1. 修复导航结束有线程未被销毁的情况

## v5.2.8.5 (2021-06-03)
1. 解决伴随路线气泡显示位置错误问题；
2. 解决实时设置路线宽度、箭头间距时，伴随路线没有生效的问题；
3. 规避自定义车标图片引起的crash问题。

## v5.2.8.4 (2021-05-25)
1. 解决切换备选路线和删除备选路线同时调用时引起的路线显示错误；
2. 解决onRouteDidChange回调不准确的问题。

## v5.2.8.1 (2021-05-08)
1. 优化了备选路线回调逻辑。
2. 解决先关闭放大图再设置放大图位置不生效的问题。
3. 若开发者监听CarNaviView地图的TencentMap#setOnPolylineClickListener(TencentMap.OnPolylineClickListener)，需在回调中调用CarNaviView#onPolylineClick(Polyline, LatLng)方法将信息同步给导航SDK。
4. 若开发者监听CarNaviView地图的TencentMap#setOnMarkerClickListener(TencentMap.OnMarkerClickListener)，需在回调中调用CarNaviView#onMarkerClick(Marker)方法将信息同步给导航SDK。

## v5.2.8.0 (2021-04-20)
1. CarNaviView新增备选路线气泡展示，新增setBackupRouteBubbleConfig() 方法可自定义气泡上的文字颜色；
2. NavigationData、AttachedLocation、BackupRoutePoint新增剩余红绿灯个数的方法getRemainTrafficLightCount()；
3. TecentNaviCallback新增获取切换平行路状态更新的回调onUpdateParallelRoadStatus()，最多可展示两个切换按钮;
4. TencentCarNaviManager新增切换平行路方法switchParallelRouteType(), 传入参数请通过上条回调获取。
