# ModAttributes 模块文档

## 模块说明
module in ModToolkit.ServerComps.ModAttributes
**本模块用于获取/设置实体自定义属性**

## 函数列表
### GetAttribute
#### 描述
获取实体自定义属性
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
from Toolkit.ServerComp import ModAttributes
ModAttributes.GetAttribute("12345", "health", "200")
```


### GetAttributes
#### 描述
批量获取实体自定义属性
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| entityId | str | 实体Id |
| \*attrNames | \*args | 变长参数，为所需要获取的实体属性名称 |

| 数据类型 | 说明 |
| -------- | ---- |
| dict | 包含请求的实体数据的字典 |

#### 示例
```python
from Toolkit.ServerComp import ModAttributes
ModAttributes.GetAttributes("12345", "health", "speed")	# 
```


### SetAttribute
#### 描述
设置实体自定义属性
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| entityId | str | 实体Id |
| name | str | 数据名称 |
| value | any |  数据值，支持一切Python基本类型|
| saveToMem | bool | 是否存入内存，默认为True |

#### 示例
```python
from Toolkit.ServerComp import ModAttributes
ModAttributes.SetAttribute("12345", "health", 20)
```


### SetAttributes
#### 描述
批量设置实体自定义属性
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| entityId | str | 实体Id |
| \*\*attrArgs | \*\*kwargs | 字典变长参数，为所需要设置的实体属性名称和对应的值 |

#### 示例
```python
from Toolkit.ServerComp import ModAttributes
ModAttributes.SetAttributes("12345", {"health": 20, "speed": 10})	# 设置实体的health为20，speed为10
```

