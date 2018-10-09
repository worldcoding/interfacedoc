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
    "dataTypeName": "透传",
    "gmtCreate": "2018-09-27",
    "model": "产品型号",
    "moduleId": "1000",
    "moduleName": "模组型号",
    "name": "门控",
    "orgName": "中天微",
    "platform": "1",
    "platformName": "阿里云",
    "productId": "1123",
    "productType": "1",
    "productTypeName": "发布",
    "typeId": "1",
    "typeName": "产品类型"
}],
    "success": true,
    "totalCount": 100
}
```

2、产品详情

```
/detail
```

请求参数示例：

```
{"productId": "1233"}
```

返回报文实体：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| name | string | 名称 |
| model | string | 型号 |
| network | string | 通讯方式 |
| platform | string | 接入平台 |
| dataType | string | 数据类型 |
| dataConvert | string | 转换脚本 |
| thingsModel | string | 物模型（json字符串） |

返回报文示例：

```
{
    "dataTypeName": "透传",
    "model": "产品型号",
    "moduleId": "1000",
    "moduleName": "模组型号",
    "name": "门控",
    "platform": "1",
    "typeId": "1",
    "dataParse": "数据解析",
    "operateDef": "功能定义",
    "protocolConvert": "协议转换",
    "remark": "描述"
}
```

3、修改产品

```
/modify
```

请求参数示例：

```
{
    "name": "门控",
    "productId": "1123",
    "dataParse": "数据解析",
    "operateDef": "功能定义",
    "protocolConvert": "协议转换",
    "remark": "描述"
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

4、新增产品

```
/add
```

请求参数示例：

```
{
    "typeId": "产品类型Id",
    "dataType": "透传",
    "model": "产品型号",
    "name": "门控",
    "moduleId": "模组型号Id",
    "platConfig": "接入配置",
    "platform": "阿里云Id",
    "remark": "描述"
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

5、删除产品

```
/delete
```

请求参数示例：

```
{"prodId":"123"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "success": true
}
```

6、获取产品列表

```
/list
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
    "name": "门控",
    "productId": "1123",
}],
    "success": true
}
```



