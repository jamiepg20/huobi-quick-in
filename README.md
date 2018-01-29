# huobi.pro市价全仓买入
效果：持续监测，上币瞬间用市场价买入

### 适用于Python3
SDK直接复制粘贴的官方推荐写法。

### 参数说明

脚本运行中可以随时调整资金，脚本会自动获取新的资金信息。

例子：打算用账户里全部未冻结的**ETH**以**市场价**购买**LUN**；

COIN1='lun'

COIN2='eth'

MIN_NUM=780 (我火币钱包里的ETH能买到780个以上的LUN才会触发本次购买)

-- 如果不想全仓买入，可以修改54行 amount='0.1' 代表购买价值0.1ETH的LUN

### 启动前的准备
在 火币PRO-我的资产-API管理 中添加一个新的API；


解压压缩包，修改 **huobi.pro-all-in\plugins\huobi\Utils.py** 中的 **ACCESS_KEY** 和 **SECRET_KEY**；

修改 **huobi.pro-all-in\all-in.py** 中的 **COIN1** 和 **COIN2**。COIN2（例如BTC）代表用来支付COIN1（例如RUFF）的币种。

打开命令行，切换到文件夹目录；

运行 `pip install -r requirements.txt`；

运行 `python all-in.py` 。

### 打赏
ETH：0x2D4866782783224076ca939687D6f62c2c247F17
