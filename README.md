# 上币监测、市价买入

[![Build Status](https://travis-ci.org/se4/huobi-all-in.svg?branch=master)](https://travis-ci.org/se4/huobi-all-in)

概括：Python3脚本持续监测huobi.pro的REST-API，在新币开放交易的瞬间用**市场价**买入

>SDK直接复制粘贴的官方推荐写法。

### 效果预览
```
任务说明>> 我想用 0.5 个 eth 来买 zla
钱包状况>> 我有 0.88 个 eth 
当前进度>> 未买到 ...
当前进度>> 未买到 ...
当前进度>> 未买到 ...
```


### 参数说明
**例子：当ZLA单价小于0.0005ETH，消耗0.5个ETH以市场价购买ZLA；**
```
COIN1 = 'zla'.lower()
COIN2 = 'eth'.lower()
COIN1_PRICE = 0.0005
COIN2_AMOUNT = 0.5
```

### 启动前的准备
在 火币PRO-我的资产-API管理 中添加一个新的API；

解压压缩包，修改 **huobi.pro-all-in\plugins\huobi\Utils.py** 中的 **ACCESS_KEY** 和 **SECRET_KEY**；

修改 **huobi-all-in\main.py** 中的 **COIN1** 和 **COIN2**。COIN2（例如BTC）代表用来支付COIN1（例如RUFF）的币种。

打开命令行，切换到文件夹目录；

运行 `pip install -r requirements.txt`；

运行 `python all-in.py` 。

### 打赏
ETH：0x2D4866782783224076ca939687D6f62c2c247F17