## 设备管理

```
/api/product/devi
```

1、设备列表

```
/pageList
```

请求参数示例：

```
{
    "condition": {
        "name": "条码",
        "userName": "hello"
    },
    "pageIndex": 1,
    "pageSize": 10
}
```

返回报文实体：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| deviceId | string | 设备信息Id |
| deviceName | string | 设备条码 |
| name | string | 所属产品 |
| userName | string | 所属用户 |
| orgName | string | 所属厂商 |
| status | string | 状态编码 |
| statusName | string | 状态名称 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "deviceId": "34343",
        "deviceName": "AAAAAAAAAA",
        "gmtCreate": "2018-09-06 21:08:32",
        "name": "门控",
        "orgName": "中天",
        "status": "1",
        "status": "正常",
        "userName": "hello"
    }],
    "success": true,
    "totalCount": 100
}
```

2、设备详情

```
/detail
```

请求参数示例：

```
{"deviceId":"223"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": {
        "deviceName": "AAAAAAAAAA",
        "gmtCreate": "2018-09-06 21:08:32",
        "name": "门控",
        "orgName": "中天",
        "status": "1",
        "statusName": "正常",
        "userName": "hello"
    },
    "success": true,
    "totalCount": 100
}
```

3、设备导入

```
/import
```

请求参数：

```
{
    "productId": "122"
}
```

4、查询设备状态

```
/status
```

请求参数示例：

```
{"deviceName":"1","productId":"2"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": {
        "status": "str",
        "name": "str"
    },
    "success": true
}
```

5、用户设备列表

```
/userDevice
```

无请求参数

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "233334",
    "result": [{
        "deviceId": "str",
        "deviceName": "str",
        "status": "str",
        "nickName": "str",
        "productId":"",
        "iconUrl":"",
        "productName":""

    }],
    "success": true
}
```

6、绑定设备

```
/bind
```

请求参数示例：

```
{"deviceName": "1"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "success": true
}
```

7、解绑设备

```
/unbind
```

请求参数示例：

```
{"deviceName": "1"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "success": true
}
```

8、轮询配置

```
/pollConfig
```

请求参数示例：

```
{
    "attrList": [""],
    "cycle": "100"
}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "success": true
}
```



