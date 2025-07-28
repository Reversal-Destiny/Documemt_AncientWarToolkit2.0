# WorldTime 模块文档

## 模块说明
module in ModToolkit.ServerComps.WorldTime
**本模块用于获取和设置主世界时间**

## 函数列表
### GetFormattedTimeStr
#### 描述
获取格式化的时间字符串
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| time | int | 时间值 |

| 数据类型 | 说明 |
| -------- | ---- |
| str | 格式化的时间值 |

#### 示例
```python
from ModToolkit.ServerComps import WorldTime
WorldTime.GetFormattedTimeStr(WorldTime.GetTime())	# 获取当前时间的格式化字符串
```


### GetGameDay
#### 描述
获取当前主世界游戏天数
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| time | int | 时间值 |

| 数据类型 | 说明 |
| -------- | ---- |
| int | 当前游戏天数 |

#### 示例
```python
from ModToolkit.ServerComps import WorldTime
WorldTime.GetGameDay(WorldTime.GetTime())	# 获取当前时间对应的游戏天数
```


### GetGameHour
#### 描述
获取当前主世界游戏时间(24小时制)
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| time | int | 时间值 |

| 数据类型 | 说明 |
| -------- | ---- |
| int | 小时数(24小时制) |

#### 示例
```python
from ModToolkit.ServerComps import WorldTime
WorldTime.GetGameHour(WorldTime.GetTime())	# 获取当前时间对应的点数
```


### GetTime
#### 描述
获取主世界时间

| 数据类型 | 说明 |
| -------- | ---- |
| int | 当前时间 |

#### 示例
```python
from ModToolkit.ServerComps import WorldTime
WorldTime.GetTime()	# 获取当前时间
```


### SetTime
#### 描述
设置主世界时间
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| time | int | 时间值 |

#### 示例
```python
from ModToolkit.ServerComps import WorldTime
WorldTime.SetTime(114514)
```

