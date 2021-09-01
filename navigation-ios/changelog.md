# Changelog

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
