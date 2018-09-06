## 设备管理

```
/api/device/devi
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
| status | string | 状态 |

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
        "status": "正常",
        "userName": "hello"
    }],
    "success": true,
    "totalCount": 100
}
```


