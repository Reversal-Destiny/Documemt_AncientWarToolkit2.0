# Attributes 模块文档

## 模块说明
module in ModToolkit.ServerComps.Attributes
**本模块用于获取/设置实体数据**

## 函数列表
### GetAttributeByName
#### 描述
通过简写名称获取实体属性
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| entityId | str | 实体Id |
| attributeName | str | 属性简写名称，可用值详见备注 |
| defaultValue | any | 初始值，支持一切Python基本类型 |

| 数据类型 | 说明 |
| -------- | ---- |
| any | 返回对应的实体数据，如果没有则返回初始值 |

#### 示例
```python
from ModToolkit.ServerComp import Attributes
Attributes.GetAttributeByName("12345", "armor", 0)
```

#### 备注
可选的属性值简写名称包括'armor'， 'speed'， 'health'， 'damage'和 'absorption'

### GetAttributes

#### 描述
批量获取实体属性
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| entityId | str | 实体Id |
| \*attributeNames | \*args | 变长参数，为所需要获取的实体属性简写名称 |

| 数据类型 | 说明 |
| -------- | ---- |
| dict | 包含请求的实体数据的字典 |

#### 示例
```python
from ModToolkit.ServerComp import Attributes
Attributes.GetAttributes("12345", "health", "speed")	# 获取实体的生命和速度属性
```


### SetAttributeByName
#### 描述
通过简写名称设置实体属性
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| entityId | str | 实体Id |
| name | str | 属性名称 |
| value | any |  数据值|

#### 示例
```python
from ModToolkit.ServerComp import Attributes
Attributes.SetAttributeByName("12345", "health", 20)
```


### SetAttributes
#### 描述
批量设置实体属性
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| entityId | str | 实体Id |
| \*\*attributeArgs | \*\*kwargs | 字典变长参数，为所需要设置的实体属性简写名称和对应的值 |

#### 示例
```python
from ModToolkit.ServerComp import Attributes
Attributes.SetAttributes("12345", {"health": 20, "speed": 10})	# 设置实体的生命值为20，速度为10
```

