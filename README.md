# huobi.pro市价全仓买入
效果：持续监测，上币瞬间用市场价买入

### 适用于Python3
SDK直接复制粘贴的官方推荐写法。

### 用法
在 火币PRO-我的资产-API管理 中添加一个新的API；


解压压缩包，修改 **huobi.pro-all-in\plugins\huobi\Utils.py** 中的 **ACCESS_KEY** 和 **SECRET_KEY**；

修改 **huobi.pro-all-in\all-in.py** 中的 **COIN1** 和 **COIN2**。COIN2（例如BTC）代表用来支付COIN1（例如RUFF）的币种。

打开命令行，切换到文件夹目录；

运行 `pip install -r requirements.txt`；

运行 `python all-in.py` 。

### 打赏
ETH：0x2D4866782783224076ca939687D6f62c2c247F17
