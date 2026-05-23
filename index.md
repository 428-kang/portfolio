# 吴康 · 数据分析作品集
![照片](images/photo.jpg)
## 项目 1：电商用户行为与转化漏斗分析

**背景**：某电商平台 11 万条用户行为日志，想找出从浏览到下单的流失瓶颈。  
**数据**：随机采样的用户访问、加购、下单流水（已脱敏），共 112,000 行。  
**工具**：Python（Pandas, Matplotlib, Plotly）、Jupyter Notebook

**分析过程：**
- 通过 `pandas` 计算整体转化漏斗：浏览 → 加购 → 下单 → 支付
- 发现 **“浏览→加购”转化仅 3.2%**，远低于行业平均
- 进一步按小时拆分，发现晚 8 点至 10 点流量最高但加购率反而最低

**关键图表：**
![整体转化漏斗](https://raw.githubusercontent.com/你的用户名/repo/main/images/funnel.png)  
*图：全站转化漏斗，加购环节流失严重*

![分时段加购率](https://raw.githubusercontent.com/你的用户名/repo/main/images/hourly_addcart.png)  
*图：各时段浏览-加购转化率，晚高峰明显下降*

**分析结论与建议：**
- 晚高峰流量多为闲逛用户，可增加限时优惠弹窗或主推爆品
- 建议对加购但未下单的用户，在 2 小时内触发优惠券推送

[📊 完整分析报告与代码](https://github.com/你的用户名/ecommerce-analysis)

---

## 项目 2：某连锁超市销售与库存优化

**背景**：超市提供 3 个月销售流水，希望优化库存结构，减少滞销品。  
**数据**：27,000 笔交易，包含商品分类、销量、库存、补货周期。  
**工具**：Python（Pandas, Seaborn）、Tableau

**分析过程：**
- 利用 `ABC 分析法` 将商品按销售额分为 A、B、C 三类
- 交叉分析库存天数，发现 C 类商品库存天数高达 48 天（远高于 A 类的 6 天）
- 用 `Seaborn` 绘制库存天数分布箱线图，识别出 12 个严重滞销单品

**关键图表：**
![ABC分类与库存天数](https://raw.githubusercontent.com/你的用户名/repo/main/images/abc_inventory.png)  
*图：各类商品平均库存天数对比，C类严重积压*

![滞销品清单](https://raw.githubusercontent.com/你的用户名/repo/main/images/deadstock.png)  
*图：滞销单品库存天数及占总库存成本比例*

**分析结论与建议：**
- 建议暂停 12 个滞销单品采购，设置库存告警线
- 引入“月均销量 < 5 且库存 > 30”的动态淘汰机制

[📊 交互式 Tableau 看板](https://public.tableau.com/你的用户名/retail)

---

## 项目 3：某健身 App 用户留存分析

**背景**：App 新用户次日留存率仅 21%，想通过行为数据定位流失点。  
**数据**：2,000 名用户首月行为日志（脱敏），含启动、课程浏览、社区互动。  
**工具**：Python、Pandas、Matplotlib

**分析过程：**
- 构建用户首月活跃天数热力图，发现第 4 天流失陡增
- 对比留存与流失用户在关键行为上的差异：留存用户平均添加 3.2 个课程，流失用户仅 0.8
- 制作留存曲线并进行群组分析

**关键图表：**
![留存曲线](https://raw.githubusercontent.com/你的用户名/repo/main/images/retention_curve.png)  
*图：不同注册周用户留存曲线，首周流失最严重*

![行为差异](https://raw.githubusercontent.com/你的用户名/repo/main/images/behavior_diff.png)  
*图：留存与流失用户前 3 天平均行为次数对比*

**分析结论与建议：**
- 引导新用户在前 3 天内完成“添加 3 个课程”任务，可有效提升留存
- 建议在第 3 天推送个性化课表，降低第 4 天流失

[📁 项目代码与数据说明](https://github.com/你的用户名/fitness-app)


