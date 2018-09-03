## 分页查询返回报文结构：

| 字段 | 类型 | 说明 |
| :--- | :--- | :--- |
| success | bool | 是否成功 |
| code | int | 错误编码 |
| message | string | 错误描述 |
| resquestId | string | 请求id，请求唯一标识 |
| result | Object | 查询返回的对象 |
| totalCount | int | 当前条件下查询到的总记录 |

## 分页查询其余业务返回报文结构：

| 字段 | 类型 | 说明 |
| :--- | :--- | :--- |
| success | bool | 是否成功 |
| code | int | 错误编码 |
| message | string | 错误描述 |
| resquestId | string |  |
| result | Object | 业务处理返回实体 |



