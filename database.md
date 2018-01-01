## Table

|Money|||
| :--- | :-- | :-- |
|category|int|类别, 0 为餐饮类，1为旅游类，2为出行类，3为医疗类，4为花费类，5为生活用品类，6为其他|
|cost|float|金额|
|time|date|记入时间|
|type|int|0为收入，1为支出|

|Budget|||
| :--- | :-- | :-- |
|init|float|原本有多少钱|
|budget|float|消费预算（默认每月1000）|
|current|float|现有金额(收入-消费)|
|left|float|距离预算还能花多少钱|

## Method

### 首页数据 SelectMainInfo()
|name|return|
| :--- | :-- |
|SelectMainInfo()|Array\<int\>|

### 返回月记录 SelectMonth(int month) 
|name|return|说明|
| :--- | :-- | :-- |
|SelectMonth()|List\<Money\>|SelectMonth(0)，参数为0时返回本月数据；<br> SelectMonth(param:1-12)  由前台控制传入参数合理（不能超过本月的月份数）

### 返回本周记录 ThisWeek()
|name|return|
| :--- | :-- |
|ThisWeek()|List\<Money\>|

### 返回年记录 SelectYear(int year) 
|name|return|说明|
| :--- | :-- | :-- |
|SelectYear()|List\<Money\>|SelectYear(0)，参数为0时返回本年数据；<br> SelectMonth(param:1-12)  由前台控制传入参数合理（不能超过本年的月年份）


### 按时间顺序返回所有流水 SelectAll()
|name|return|
| :--- | :-- |
|SelectAll()|List\<Money\>|


### 返回最新一笔消费 SelectLatest()
|name|return|
| :--- | :-- |
|SelectLatest()|List\<Money\>|

### 返回日收入/支出 TodaySum()
|name|return|说明|
| :--- | :-- |:-- |
|TodaySum()|float[]|数组中[0] 为总收入，[1] 为总支出|

### 返回本周收入/支出 ThisWeekSum()
|name|return|说明|
| :--- | :-- |:-- |
|ThisWeekSum()|float[]|数组中[0] 为总收入，[1] 为总支出|

### 返回本月收入/支出 ThisMonthSum()
|name|return|说明|
| :--- | :-- |:-- |
|ThisMonthSum()|float[]|数组中[0] 为总收入，[1] 为总支出|

### 返回首页信息[冗余] SelectMainInfo() 
|name|return|说明|
| :--- | :-- |:-- |
|SelectMainInfo()|float[]|[0] latest 收入 <br> [1] latest 支出 <br> [2] 本周 收入 <br> [3] 本周 支出 <br> [4] 本月 收入 <br> [5] 本月 支出 <br> [6] 今日 收入 <br> [7] 今日 支出 <br> [8] 余额(未写) <br>|

### 各月份按种类的收入/支出 SelectType(int month, int category)
|name|return|说明|
| :--- | :-- |:-- |
|SelectType(int month, int category)|float[]|数组中[0] 为收入，[1] 为支出<br>SelectType(0, 1) // 月份参数为0时返回本月, category 为1时为旅游类<br>SelectType(param:1-12,param:0-6) 前台控制传入参数合理<br>|








