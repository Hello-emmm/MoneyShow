|User|||
| :--- | :-- | :-- |
|id|string|
|name|string|


|Record|||
| :--- | :-- | :-- |
|category|int|类别|
|payment|int|0为现金,1为支付宝,2为信用卡|
|cost|int|金额|
|userid|string|User->id|
|time|date|记入时间|
|type|int|0为收入，1为支出|

|Budget|||
| :--- | :-- | :-- |
|userid|string|User->id|
|cost|int|消费预算（默认每月1000）|
