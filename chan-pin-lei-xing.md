## 产品类型

```
/api/base/prodType
```

1、名称查询

```
/pageList
```

请求参数示例：

```
{
    "name": "灯",
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
        "typeId": "12233",
        "name": "灯",
        "code": "DENG",
        "remark": "物模型"
    }],
    "success": true,
    "totalCount": 100
}
```

2、新增类型

```
/add
```

请求参数示例：

```
{
    "name": "灯",
    "code": "deng",
    "remark": "物模型"
}
```



