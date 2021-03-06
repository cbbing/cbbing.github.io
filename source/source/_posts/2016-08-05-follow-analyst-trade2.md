---
layout: post
title: 跟着分析师炒股系列（二）
date: 2016-08-05 09:10:42
tags:
	- 大数据
	- 股票
category: Finance
comments: true
---

在系列第一篇《[跟着分析师炒股系列（一）](http://kekefund.com/2016/07/25/follow-analyst-trade/)》里，信谁大数据科学团队以分析师研报推荐的股票池，建立了一套股票组合轮动的交易策略，发掘出累积收益最高的一票分析师，其中最牛的招商证券分析师刘荣的累积收益竟达80倍！

不过，累积收益还可能包含运气成分，比如大牛市下推荐股票都大涨，还不能算真英雄。这一次我们来看看相对收益，看能不能找出穿越牛熊的分析师，尤其是最近一年熊市震荡下他们的表现如何。

延续上一篇的交易策略，筛选分析师评级为买入和增持的股票，形成股票池。
调仓周期为3个月。
选取分析师评级为“买入、增持”的股票。实现3个月一轮换。
<!-- more -->
具体在每三个月的月末，选取最近发表三篇研报推荐的股票：
- 若三只股票与前三个月推荐的完全一样，则继续持有；
- 若三只股票都不一样，则卖掉所有持仓，买入新推荐的三只股票；
- 若三只股票有一到两只不同，则卖掉收益率最高的持仓股票，买入新推荐的一到两只股票。

---

# 一，年化相对收益率排名TOP10

我们挑选最近活跃的分析师（在1年内有发表研报），并且其交易周期≥1年。共747名分析师，先看结果：

![](http://7xo67b.com1.z0.glb.clouddn.com/2016-08-05/trade2_1.png)



> 注：相对收益率对比基准是上证指数

相对收益率看的是真本事，不论牛熊，能真正跑赢大盘的才是真正的王者。其中，招商证券电气设备新能源行业分析师胡毅取得第一名，相对年收益率为125.7%。这与他主攻研究储能与新能源电池产业，也有很大关系，从热门板块中发掘优质个股。



# 二，最近热门分析师相对收益率

眼下，相信大家最关心的就是震荡市选股问题，如何在大势不好的情况下选出黑马股跑赢大盘。来看看2015年6月15日股灾过后，分析师们的表现如何？在这近1年的震荡中有没有战胜大势的分析师？
挑选标准：
- 最近1年研报数量>=10
- 最后一次发表研报在近6个月
 
按此标准，共筛选出符合要求的分析师693名。
## 近一年最高年化相对收益率排名：

![](http://7xo67b.com1.z0.glb.clouddn.com/2016-08-05/trade2_2.png)


> 注：最大相对收益率越大越好，最大回撤率越低越好。

最近一直是震荡行情，能在震荡行情实现较高的相对收益率，这样的分析师具备较高的选股能力。排名第一的是广发证券巨国贤分析师，年化相对收益率达到来 202.8%！
但他在信谁平台上的“言值”并不高，言值为58。这是为什么呢？
翻看巨国贤的履历，他从2007年转型进入证券行业，并在13年、14年拿到有色金属行业新财富最佳分析师，还被业界称为“大气晚成型”。言值低，就因为之前的荐股错误较多。对于这样历史表现不佳，而最近崛起的“黑马”分析师，我们可以格外关注。
![](http://7xo67b.com1.z0.glb.clouddn.com/2016-08-05/trade2_3.png)

来看看他的调仓记录：（初始资金设置为100万）

## 第1次调仓

|交易日期|股票代码|操作|成交数量|成交价格|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|2015-07-30|赤峰黄金(600988)|买入|25500|13.06|
|2015-07-30|众和股份(002070)|买入|34300|9.70|

当前市值：100000， 盈亏比例：0%

## 第2次调仓

|交易日期|股票代码|操作|成交数量|成交价格|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|2015-10-30|赤峰黄金(600988)|卖出| 25500 |12.73| 
|2015-10-30|众和股份(002070)|卖出|34300|17.6|
|2015-10-30|宝钛股份(600456)|买入|18600|17.9|
|2015-10-30|赣锋锂业(002460)|买入|19200|16.99|
|2015-10-30|融捷股份(002192)|买入|29100|20.73|

当前市值：1262555， 盈亏比例：26..3%

> 注：002070由于停牌无法卖出，推迟到2015-12-07交易。

## 第3次调仓

|交易日期|股票代码|操作|成交数量|成交价格|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|2016-01-28|赣锋锂业(002460)|卖出|19200|16.68|
|2016-01-28|融捷股份(002192)|卖出|16200|24.8|
|2016-01-28|豫光金铅(600531)|买入|165500|4.36|

当前市值：1313868， 盈亏比例：31.4%

## 第4次调仓

|交易日期|股票代码|操作|成交数量|成交价格|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|2016-04-28|宝钛股份(600456)|卖出|18600|16.3|
|2016-04-28|融捷股份(002192)|卖出|12900|42.12|
|2016-04-28|豫光金铅(600531)|卖出|165500|8.41|
|2016-04-28|正海磁材(300224)|买入|15700|19.29|
|2016-04-28|云海金属(002182)|买入|90700|15.35|
|2016-04-28|天齐锂业(002466)|买入|12700|42.69|

当前市值：2238983， 盈亏比例：123.9%

## 第5次调仓

|交易日期|股票代码|操作|成交数量|成交价格|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|2016-07-27|正海磁材(300224)|卖出|15700|20.58|
|2016-07-27|云海金属(002182)|卖出|90700|22.0|
|2016-07-27|天齐锂业(002466)|卖出|12700|39.15|

当前市值：2817433， 盈亏比例：181.7%

期间大盘跌了19%，其相对年化收益率为202.8%。


## 高言值分析师与低言值分析师收益率对比：

![](http://7xo67b.com1.z0.glb.clouddn.com/2016-08-05/trade2_4.png)


> 注：最大相对收益率越大越好，最大回撤率越低越好。

从上面的散点图可以看出，高言值的分析师策略取得正收益的概率比低言值的高，但是收益率越高，风险越大（最大回撤率越大）。


# 三，分析师神推荐股票

## 2016年分析师推荐股票次数排名TOP10

|股票名称|股票代码|推荐次数|涨幅（%）
|:-:|:-:|:-:|:-:|
|隆基股份|601012|104|19.3|
|美的集团|000333|102|47.9|
|贵州茅台|600519|85|49.1|
|阳光电源|300274|84|-7.8|
|国轩高科|002074|83|10.6|
|华策影视|300133|83|-15.1|
|网宿科技|300017|81|38.2|
|沧州明珠|002108|78|51.3|
|老板电器|002508|76|46.4|
|宋城演艺|300144|74|-12.0|

> 注：收益率计算截止到7月31日

可见，推荐次数排名前十的股票，有7只上涨，3只下跌；上涨的平均收益为37.5%，下跌的平均亏损为-11.6%。



按最简单的均分法，将资金等额购买这10只股票，就能取得22.8%的收益率！而大盘今年截止目前跌幅是9.61%。



看样子，对于“懒人”投资者，直接跟着这个统计规律买卖的话也能战胜大盘！这背后其实是专业分析的力量，当分析师一致看好的时候，黑马股的概率更大。



# 四、分析师研报特点
对券商分析师研报分析，发现分析师最爱的评级是增持和买入，占到83.65%。
远大于评级为“卖出”和“减持”的数量。 
![](http://7xo67b.com1.z0.glb.clouddn.com/2016-08-05/trade2_5.png)


你懂的，这就是卖方分析师的命脉，在A股现有投资氛围下唱多更容易受机构和投资者待见。

喜欢唱多不要紧，问题是真的符合评级的有多少，这就是信谁分析师言值评价的作用。


就像业内的传说：
> 据前辈口口相传，在那遥远的地方，有一群苦逼的策略分析师，日出而作，月落不息，苦练 《葵花宝典》和《屠龙刀法》，希望有朝一日能够在‘新财富’杯华山论剑中一举发威、技惊四座。能入行的，没有笨人。能入门的，没有懒人。想拿奖？唯有能拼命的猛人。

