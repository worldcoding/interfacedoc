## 设备上下线日志

```
/api/product/onOff
```

1、设备上下线日志分页列表

```
/pageList
```

请求参数示例：

```
{
    "condition": {
        "beginDate": "2018-09-06",
        "endDate": "2018-09-06",
        "name": "门控",
        "userName": "hello"
    },
    "pageIndex": 1,
    "pageSize": 10
}
```

返回报文实体：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| name | string | 设备名称 |
| userName | string | 用户名 |
| productName | string | 产品名称 |
| status | string | 状态 |
| statusName | string | 状态名称 |
| time | string | 时长 |
| gmtCreate | string | 发生时间 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "gmtCreate": "2018-09-06 19:08:22",
        "name": "门控",
        "orgName": "中天",
        "productName": "门控",
        "status": "1",
        "statusName": "在线",
        "time": "12",
        "userName": "hello"
    }],
    "success": true,
    "totalCount": 100
}
```

2、设备上线日志列表

```
/list
```

请求参数示例：

```
{
    "beginDate": "2018-09-06",
    "endDate": "2018-09-06",
    "deviceId": 1
}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "gmtCreate": "2018-09-06 19:08:22",
        "status": "1",
        "statusName": "在线"
        "time": "12"
    }],
    "success": true
}
```



