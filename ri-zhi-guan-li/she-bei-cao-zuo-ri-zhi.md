## 设备操作日志

```
/api/device/log
```

1、操作日志列表

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
        "message": "在线",
        "userName": "hello"
    }],
    "success": true,
    "totalCount": 100
}
```



