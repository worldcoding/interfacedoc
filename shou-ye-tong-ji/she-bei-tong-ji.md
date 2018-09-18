## 设备统计

```
/api/device/diagram
```

1、dayNum天日均设备活跃数量，默认90天

```
/active
```

请求参数示例：

```
{"dayNum":"90"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "regDate": "2018-09-04 12:32:20",
        "userNum": "10"
    }],
    "success": true
}
```



