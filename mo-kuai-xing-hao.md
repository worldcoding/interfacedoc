## 模块型号

```
/api/base/module
```

1、模块型号查询

```
/pageList
```

请求参数示例：

```
{
    "name": "CP6702-WIFI",
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
        "gmtCreate": "2018-09-04 12:32:20",
        "modelId": "12233",
        "model": "CP6702-WIFI",
        "type": "DTU",
        "network": "0",
        "networkName": "WIFI",
        "config": "配置内容"
    }],
    "success": true,
    "totalCount": 100
}
```

2、模组型号列表

```
/list
```

无请求参数

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "modelId": "12233",
        "model": "CP6702-WIFI",
        "type": "DTU"
    }],
    "success": true
}
```

3、新增模组型号

```
/add
```

请求参数示例：

```
{
    "model": "CP6702-WIFI",
    "type": "DTU",
    "network": "0",
    "networkName": "WIFI",
    "config": "配置内容"
}
```

4、修改

