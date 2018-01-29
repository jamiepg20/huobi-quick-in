# 上币监测、市价全仓买入

[![Build Status](https://travis-ci.org/se4/huobi-all-in.svg?branch=master)](https://travis-ci.org/se4/huobi-all-in)

效果：持续监测火币PRO的REST-API，在新币开放交易的瞬间用**市场价**买入

### 适用于Python3
SDK直接复制粘贴的官方推荐写法。

脚本运行中可以随时调整资金，脚本会自动获取新的资金信息。

### 参数说明
**例子：打算用钱包里全部ETH以市场价购买LUN**

```
COIN1='lun'
COIN2='eth'
MIN_NUM=5

-- 我火币钱包里的ETH能买到5个以上的LUN才会触发本次购买
-- 如果不想全仓买入，可以修改54行 amount='0.1' 代表购买价值0.1ETH的LUN
```

### 启动前的准备
在 火币PRO-我的资产-API管理 中添加一个新的API；


解压压缩包，修改 **huobi.pro-all-in\plugins\huobi\Utils.py** 中的 **ACCESS_KEY** 和 **SECRET_KEY**；

修改 **huobi.pro-all-in\all-in.py** 中的 **COIN1** 和 **COIN2**。COIN2（例如BTC）代表用来支付COIN1（例如RUFF）的币种。

打开命令行，切换到文件夹目录；

运行 `pip install -r requirements.txt`；

运行 `python all-in.py` 。

### 打赏
ETH：0x2D4866782783224076ca939687D6f62c2c247F17