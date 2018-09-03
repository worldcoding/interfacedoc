# 角色管理\(/api/base/sysRole\)

1、角色分页列表\(/pageList\)

请求参数：

| 字段 | 类型 | 名称 | 说明 |
| :--- | :--- | :--- | :--- |
| pageIndex | string | 页面索引 | 大于0的数字 |
| pageSize | string | 分页大小 | 大于0的数字 |
| name | string | 角色名称 | 可为空 |

请求参数示例：

```
{
    "name": "管理员",
    "pageIndex": "1",
    "pageSize": "10"
}
```

返回参数：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| code | string | 错误编码 |
| success | bool | 是否成功 |
| message | string | 错误描述 |
| resquestId | string | 请求id，请求唯一标识 |
|  |  |  |



