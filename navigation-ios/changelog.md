# iOS导航SDK Changelog

## v5.3.4 (2021-11-29)
1.	重构导航服务数据序列化反序列化模块。
2. 优化电子眼展示，支持最多3排展示。
3. 优化放大图预下载机制。
4. 优化伴随气泡展示位置。
5. 更新导航路线上的红绿灯图片资源，展示效果更佳。
6. 调整CarNaviView默认的最小比例尺，从14调整为15。

## v5.3.3 (2021-10-29)
1.	TNKCarNaviManager新增导航中修改算路策略方法(changeSearchOptions:);
2. TNKCarRouteSearchOption新增算路策略：是否大路优先(bigRoad)、是否优先时间短(shortTime)、是否优先高速(highway)；
3. TNKCarNaviUIDelegate新增回调：carNavigationManager:showGuidedLaneInfo:，展示车道线时提供扩展信息；
4. TNKCarSearchOptions新增参数initialRouteID、initialNaviSessionID用于乘客选路功能。


## v5.3.2 (2021-09-27)
1.	TNKSearchNaviPoi新增searchNaviPoiType字段。开发者可选择起终点参数是否使用区域面反查POI策略
2.	TNKCarNaviManager新增changeDestination:wayPoints:方法，导航过程可同时修改终点、途径点;
3.	TNKCarNaviView新增enlargedIntersectionAspect字段，路口放大图可修改宽高比;
4.	补齐限停摄像头;
5.	TNKSearchNaviPoi算路起终点新增poiName字段，允许开发者传入，该参数暂不影响算路策略


## v5.3.1 (2021-09-01)
1. 新增导航过程修改途径点接口;
2. 新增导航过程中修改目的地接口；
3. 路径规划返回红绿灯数据，导航地图展示路线上的红绿灯。


## v5.3.0 (2021-07-30)
1. 更新了导航引擎，提升整体导航体验


## v5.2.9.6 (2021-07-15)
1. 优化自动比例尺缩放的路口增强策略；
2. TNKCarNaviView新增autoScaleMinZoomLevel字段，开发者可以设置导航过程中3D导航模式自动比例的最小zoomlevel值。

## v5.2.9 (2021-06-30)
1. 优化自动比例尺缩放功能；
2. 优化语音播报功能；
3. 优化路径规划服务耗时；
4. 优化导航过程的回弹模式。


## v5.2.8.2 (2021-06-25)
1. 解决切换备选路线和删除备选路线同时调用时引起的路线显示错误；
2. 解决默认导航面板样式错误问题；
3. 解决杀掉进程偶现收到crash信息。

## v5.2.8.1 (2021-05-08)
1. 优化了备选路线回调逻辑。

## v5.2.8 (2021-04-20)
1. TNKCarNaviView新增备选路线气泡展示，新增backupRouteBubbleConfig属性可自定义气泡上的文字颜色；
2. TNKCarNavigationData、TNKLocation、TNKBackupRouteLocation新增剩余红绿灯个数的字段remainTrafficLightCount；
3. TNKCarNaviDelegate新增获取切换平行路状态更新的回调4. carNavigationManager:updateParallelRoadStatus:，最多可展示两个切换按钮;
4. TNKCarNaviManager新增切换平行路方法switchParallelRouteType:, 传入参数请通过上条回调获取;
5. 修复bug: 当展示路口放大图时发生偏航，路口放大图消失但是没有放大图消失回调。
