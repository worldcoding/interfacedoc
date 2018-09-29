## 在线调试

```
/api/product/online
```

1、物模型和设备数据转换

```
/convert
```

请求参数：

| 类型 | 名称 | 说明 |
| :--- | :--- | :--- |
| int | 命令类型 | 1：控制命令；2：轮询配置 |
| int | 转换类型 | 1：物模型-&gt;设备数据；2：设备数据-&gt;物模型 |
| String | 输入命令 |  |
| String | 产品id |  |

请求参数示例：

```
{
    "cmdType": 1,
    "convertType": 1,
    "inputCmd": "{\"act\":6,\"body\":{\"switch\":\"1\"},\"seq\":\"3565755380170489856\"}",
    "productId": "223242"
}
```

返回报文结构：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": "{"act":6,"body":[{"type":"gpio-1","id":0,"cmd":
    [1,0,-24,1,0,0,0,0,0,0,2,0,0,0,0,1]}],"seq":"3565755380170489856"}",
    "success": true
}
```

2、命令调试

```
/debug
```

请求参数示例：

```
{
    "cmdStr": "{\"act\":6,\"body\":{\"switch\":\"1\"},\"seq\":\"3565755380170489856\"}",
    "cmdType": 1, 
    "deviceName": "csky0001",
    "productId": "10000"
}
```

```
cmdType：1：控制命令；2：轮询配置
```

返回报文结构：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": {"commandId": "1123"}
    "success": true
}
```

返回成功表示命令成功接收

调试日志异步提供

调试日志websocket地址：

```
/socket/product/debug/{userId}
```

推送报文结构：

```
{
    "cmdLogInfo": {
        "content": "{\"switch\":\"1\"}",
        "deviceId": "csky10001",
        "deviceName": "csky10001",
        "gmtCreate": "2018-09-29 11:48:31",
        "model": "d233",
        "msgType": "1",
        "name": "灯",
        "orgId": "1000",
        "orgName": "中天",
        "userId": "10000",
        "userName": "test"
    },
    "commandId": "1123",
    "errCode": 0,
    "errMsg": "",
    "success": true
}
```



