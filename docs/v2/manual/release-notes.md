# 产品更新日志

我们的精益迭代助力您的精益成长！

## 2019年1月

### V4.1.1 @20190124

#### 新增

- 新增了[短信推送](./operation-sms.md)，支持自定义分群发送营销短信
- 新增了独立的 [Session 分析](.analytics-session.md)模型，从事件分析当中独立出来，更便捷的分析用户连续的行为、不同频次或时长的用户分布；
- 新增了[监控告警](.project-monitoring.md)，支持自定义监控关键指标，当指标达到设定阈值时自动发送告警消息，查看异常情况

#### 优化

- 优化了漏斗计算的准确性，重复事件时提升到毫秒级别计算漏斗转化
- 优化了数据缓存，超过阀值自动强制刷新缓存数据
- 优化了自动登录时的体验

#### Bug修复

- 修复了部分情况下用户属性上报缺失的情况

### V4.1.0 @20190108

#### 新增

- 新增了[广告跟踪](./operation-utm.md)的功能
   * 支持批量上传生成跟踪链接
   * 支持批量下载生成后的链接
   * 支持链接时同时生成带参数的二维码（可自定义 LOGO 和尺寸）
   * 单条创建支持下拉选择广告来源和媒介，也支持自定义来源和媒介
   * 单条创建时支持在当前页继续生成新的链接
   * 支持增加备注
   * 支持删除无效链接
   * 支持查看单条链接的指标表现
- 新增了预置分群：新访问用户 和 新注册用户 ，支持在各个分析模型中对比分析
- 新增了实验室（用于承载一些实验性功能）

#### 优化

- 优化了主导航，移入分析 、运营 和 管理 可以快速切换二级导航
- 拆分了[消息通知](./operation-pushmessage.md)和[电子邮件](./operation-email.md)  ，可以从二级导航进入，更方便管理和创建邮件
- 优化了分群推送时直接选择消息通知还是电子邮件
- 优化了点击图表元素时popup菜单位置，使得数据标签完整出现在可视范围内
- 优化了事件分析多个指标时默认的图表
- 优化了事件分析中数值型图表添加看板时widget可控制的大小
- 优化了元事件列表中不包含属性的事件行效果（去掉了箭头，不支持点击展开）
- 优化了小舟助手位置，使得不遮挡主功能
- 优化了按照平台维度细分时显示的维度值，变得更易读

#### SDK 和开放平台

- 新增了PHP SDK
- SDK 首次访问时间 $first_visit_time 强制转化为东八区，方便数据统一处理
- 新增了presto-kafka插件，支持通过presto查询kafka中的数据
- 邮件发送服务支持 SSL

#### Bug修复

- 修复了事件分析-自定义指标表格模式未显示单位的问题
- 修复了首次创建项目后，不刷新页面不显示进入产品的入口
- 修复了自定义指标分享给其他用户时，显示的为 code 而不是名称的问题
- 修复了数据中非广告系列的问题
- 修复了单机版无法启动数据流的问题
- 修复了部分情况下用户属性上报缺失的情况