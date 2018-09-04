## 字典管理

```
/api/base/dict
```

1、字典分页列表

```
/pageList
```

请求参数示例：

```
{
    "name": "日志管理",
    "pageIndex": 1,
    "pageSize": 10
}
```

返回实体结构：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| dectId | string | 字典Id |
| name | string | 字典名称 |
| type | string | 类型 |
| code | string | 字典码 |
| value | string | 字典值 |
| orderNum | string | 排序字段 |
| remark | string | 说明 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "code": "0",
        "dectId": "13",
        "name": "性别",
        "orderNum": "1",
        "remark": "备注",
        "type": "sex",
        "value": "女"
    }],
    "success": true,
    "totalCount": 100
}
```

3、新增字典

```
/add
```

请求参数：

| 字段 | 类型 | 名称 | 说明 |
| :--- | :--- | :--- | :--- |
| name | string | 字典名称 |  |
| type | string | 类型 |  |
| code | string | 字典码 |  |
| value | string | 字典值 |  |
| orderNum | string | 排序字段 |  |
| remark | string | 说明 |  |

请求参数示例：

```
{
    "code": "0",
    "name": "性别",
    "orderNum": "1",
    "remark": "备注",
    "type": "sex",
    "value": "女"
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

4、修改字典

```
/modify
```

请求参数说明同新增

请求参数示例：

```
{
    "dectId":"123",
    "code": "0",
    "name": "性别",
    "orderNum": "1",
    "remark": "备注",
    "type": "sex",
    "value": "女"
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

5、删除字典

```
/delete
```

请求参数示例：

```
{"dectId":"12333"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "success": true
}
```

6、根据字典类型获取字典编码和value列表

```
/dictList
```

请求参数示例：

```
{"type","sex"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "code": "0",
        "name": "性别",
        "value": "女"
    }],
    "success": true
}
```



