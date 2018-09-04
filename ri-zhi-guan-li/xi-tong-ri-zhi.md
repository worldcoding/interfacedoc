## 系统日志

```
/api/base/log
```

1、日志分页列表

```
/sysLogPageList
```

请求参数：

| 字段 | 类型 | 名称 | 说明 |
| :--- | :--- | :--- | :--- |
| pageIndex | int |  |  |
| pageSize | int |  |  |
| condition | Object | 检索条件 |  |
| condition.name | string | 帐号 |  |
| condition.beginDate | string | 日志创建开始时间 | 格式：2018-09-04 |
| conditon.endDate | string | 日志创建结束时间 |  |

请求参数示例：

```
{
    "condition": {
        "name": "hello",
        "beginDate": "2018-09-04",
        "endDate": "2018-0904"
    },
    "pageIndex": 1,
    "pageSize": 10
}
```

返回实体结构：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| operation | string | 操作 |
| methond | string | 方法名称 |
| params | string | 参数 |
| time | string | 执行时长 |
| ip | string | ip地址 |
| name | string | 帐号 |
| userName | string | 用户名 |
| gtmCreate | string | 日志生成时间 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "gmtCreate": "2018-09-04 12:32:20",
        "ip": "192.168.168.24",
        "method": "getUserList",
        "name": "中天",
        "operation": "查询用户信息",
        "params": "2222",
        "time": "232",
        "username": "hello"
    }],
    "success": true,
    "totalCount": 100
}
```



