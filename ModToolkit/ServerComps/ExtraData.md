# ExtraData 模块文档

## 模块说明
module in ModToolkit.ServerComps.ExtraData

**本模块用于获取/设置实体或世界的自定义数据**

## 函数列表
### GetEntityData
#### 描述
获取实体数据
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| entityId | str | 实体Id |
| name | str | 数据名称 |
| defaultValue | any | 初始值，支持一切Python基本类型 |

| 数据类型 | 说明 |
| -------- | ---- |
| any | 返回对应的实体数据，如果没有则返回初始值 |

#### 示例
```python
from ModToolkit.ServerComps import ExtraData
ExtraData.GetEntityData("1234", "team_name", "china")
```


### GetWorldData
#### 描述
获取世界数据
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| name | str | 数据名称 |
| defaultValue | any |  初始值，支持一切Python基本类型|

| 数据类型 | 说明 |
| -------- | ---- |
| any |  返回对应的世界数据，如果没有则返回初始值|

#### 示例
```python
from ModToolkit.ServerComps import ExtraData
ExtraData.GetWorldData("levelId", "-1")
```


### SetEntityData
#### 描述
设置实体数据
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| entityId | str | 实体Id |
| name | str | 数据名称 |
| value | any |  数据值，支持一切Python基本类型|
| saveToMem | bool | 是否存入内存，默认为True |

#### 示例
```python
from ModToolkit.ServerComps import ExtraData
ExtraData.SetEntityData("12345", "team_name", "japan")
```


### SetWorldData
#### 描述
设置世界数据
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| name | str | 数据名称 |
| value | any |  数据值，支持一切Python基本类型|
| saveToMem | bool | 是否存入内存，默认为True |


#### 示例
```python
from ModToolkit.ServerComps import ExtraData
ExtraData.SetWorldData("levelId", "12345")
```

