# Message 模块文档

## 模块说明
module in ModToolkit.ServerComps.Message
**本模块用于**发送消息

## 函数列表
### NotifyMesssage
#### 描述
向指定玩家发送通知消息（悬浮提示）

| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| playerId | str | 接收消息的玩家实体ID |
| msg | str | 需要显示的消息内容 |
| color | str | 消息文本颜色代码（使用TextColor类中的常量） |

#### 示例
```python
from ModToolkit.ServerComp import Message

Message.NotifyMesssage("12345", "任务已完成！", "§2")
```


### SendErrorNotice
#### 描述
发送错误通知（红色[ERROR]前缀）

| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| playerId | str | 接收消息的玩家实体ID |
| msg | str | 需要显示的消息内容 |

#### 示例
```python
from ModToolkit.ServerComp import Message
Message.SendErrorNotice("12345", "背包已满！")
```


### SendInfoNotice
#### 描述
发送普通信息通知（黄色[INFO]前缀）

| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| playerId | str | 接收消息的玩家实体ID |
| msg | str | 需要显示的消息内容 |

#### 示例
```python
from ModToolkit.ServerComp import Message
Message.SendInfoNotice("12345", "背包快满了！")
```


### SendSystemNotice
#### 描述
发送系统级通知（绿色[SYS]前缀）

| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| playerId | str | 接收消息的玩家实体ID |
| msg | str | 需要显示的消息内容 |

#### 示例
```python
from ModToolkit.ServerComp import Message
Message.SendSystemNotice("12345", "系统加载完成")
```


### SendWarningNotice
#### 描述
发送警告通知（金色[WARNING]前缀）
| 参数名 | 数据类型 | 说明 |
| ------ | -------- | ---- |
| playerId | str | 接收消息的玩家实体ID |
| msg | str | 需要显示的消息内容 |

#### 示例
```python
from ModToolkit.ServerComp import Message
Message.SendWarningNotice("12345", "你没血了！")
```

