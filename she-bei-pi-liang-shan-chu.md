1、批次查询

```
/api/product/batch/pageList
```

请求参数示例：

```
{
    "condition": {
        "fileName": "str",
        "beginDate": "2018-12-14",
        "endDate": "2018-12-17"
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
        "batchId": "str",
        "userName": "str",
        "gmtImport": 1545012868044,
        "fileName": "str",
        "productName": "str",
        "count": 0,
        "status": 0
    }],
    "success": true,
    "totalCount": 100
}
```

2、批量删除

```
/api/product/devi/batchDelete
```

请求参数示例：

```
{"batchId":"123"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "success": true
}
```

3、设备key下载

```
/api/product/devi/download
```

请求参数示例：

```
{"batchId":"123"}
```



