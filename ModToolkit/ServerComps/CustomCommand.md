# CustomCommand 模块文档

## 模块说明
module in ModToolkit.ServerComps.CustomCommand
**本模块用于判断自定义指令是否可被正确执行(参数是否足够、值是否在给定范围内)**

## 函数列表
### GetArgs
#### 描述
解析自定义指令参数
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| args | list(dict) | 自定义命令参数，详见备注 |
| expected_arg_count | int | 参数数量 |
| argsRange | dict | 参数范围 |

| 数据类型 | 说明 |
| -------- | ---- |
| dict | 获取状态及解析到的值，详见备注 |

#### 示例
```python
from ModToolkit.ServerComp import CustomCommand
@Listener
def CustomCommandTriggerServerEvent(self, args):
    command = args["command"]
    _args = args["args"]
    user_args = CustomCommand.GetArgs(_args,1,{"value": (1, 2, 3, 4)})
```
#### 备注
- 自定义命令参数备注如下
本方法一般配合CustomCommandTriggerServerEvent一起使用，args值一般为CustomCommandTriggerServerEvent中的`args["args"]`
- 获取状态及解析到的值备注如下
| 键 |  类型 |说明 |
| ----- | ---- | ------- |
| success |bool | 解析状态，如果失败返回False |
| message |string | 解析失败时才会包含的参数，为失败的原因 |
| \*\*keys |dict | 解析成功时会直接以args中的键为键，值为获取到的值 |

### VerifyCommandLength
#### 描述
验证自定义指令参数是否符合预设数量及范围
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| args | list(dict) | 自定义命令参数 |
| numOfArgs | int | 参数数量 |
| argsRange | dict | 参数范围 |

| 数据类型 | 说明 |
| -------- | ---- |
| bool | 是否通过验证 |

#### 示例
```python
from ModToolkit.ServerComp import CustomCommand
@Listener
def CustomCommandTriggerServerEvent(self, args):
    command = args["command"]
    _args = args["args"]
    print CustomCommand.VerifyCommandLength(_args,1,{"value": (1, 2, 3, 4)})
```

