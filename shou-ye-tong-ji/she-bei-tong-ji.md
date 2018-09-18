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
        "activeDate": "2018-09-04 12:32:20",
        "deviceNum": "10"
    }],
    "success": true
}
```

2、设备分类统计

```
/count
```

无请求参数

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": {
        "dev_sum": "设备总数",
        "online": "在线数量",
        "offline": "离线数量",
        "active": "激活数量",
        "prod_kind": "产品种类"
    },
    "success": true
}
```

3、设备实时状态

```
/actual
```

请求参数示例：

```
{"num","20"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "date": "2018-09-04 12:32:20",
        "status": "上线",
        "name: "名称"
    }],
    "success": true
}
```



