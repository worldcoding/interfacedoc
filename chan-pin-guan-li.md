## 产品管理

```
/api/product/prod
```

1、产品分页列表

```
/pageList
```

请求参数示例：

```
{
    "name": "中天",
    "pageIndex": 1,
    "pageSize": 10
}
```

返回报文实体结构：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| productId | string | 产品id |
| name | string | 名称 |
| model | string | 产品型号 |
| network | string | 通讯方式 |
| networkName | string | 通讯方式名称 |
| platform | string | 接入平台 |
| platformName | string | 平台名称 |
| datatType | string | 数据类型 |
| dataTypeName | string | 数据类型名称 |
| orgName | string | 所属厂商 |
| productType | string | 产品状态 |
| productTypeName | string | 产品状态描述 |
| gmtCreate | string | 添加时间 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "gmtCreate": "2018-09-04 12:32:20",
        "productId": "12233",
        "name": "庭院门控",
        "model": "产品型号",
        "network": "1",
        "networkName": "4G",
        "platform": "0",
        "platformName": "阿里云",
        "dataType": "1",
        "dataTypeName": "透传"
        "orgName": "中天",
        "productType":"0",
        "productTypeName": "发布"
    }],
    "success": true,
    "totalCount": 100
}
```

2、产品详情

```
/detail
```



