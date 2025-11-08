## 期货合约

### 数据

私有数据 跟用户相关，需要登录
公有数据

#### 公有数据

公共行情数据

- 市场行情信息
  - minTicker
    - lasPrice 最新价
    - markPrice 标记价格 用于 合约 公允价格，计算资金费率，使得合约价格不至于偏离现货价格太远
    - indexPrice 指数价格，用于 现货 公允价格 取不同交易所 加权平均 
  - 24Tickers
    - 24hr 最高最低价
    - 24hr 成交量
    - miniTicker
  - kline 历史成交
  - orderBook  委托


#### 私有数据
需要登录跟个人相关

- 个人仓位
  - positions
- 用户信息
  - setting
- 资产信息
  - wallet

### 数据变化很快

快照 某一时刻 的数据
推送 实时数据

http 先是请求一遍快照，一般是全量数据
ws 推送增量数据，进行增删改

一般是 redux / zustand

按照 nameSpace 存储各个模块的数据

lastUpdateId = lastUpdateId + 3

orderBook
增量数据
补号 请求一遍快照 
que [变化数据] + 推送
全量数据

仓位
部分成交/全部成交
position 0.1 

保证金 全仓 全部仓位


#### 库

decimal.js 处理数字加减乘除

多语言 变量替换 
in18n-next
key
weblate
crodein


