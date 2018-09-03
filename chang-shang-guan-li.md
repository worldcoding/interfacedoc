## 厂商管理

```
/api/base/sysOrg
```

1、厂商分页列表

```
/pageList
```

请求参数示例：

```
{
    "name": "中天",
    "pageIndex": "1",
    "pageSize": "10"
}
```

返回报文实体结构：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| orgId | string | 厂商id |
| parentId | string | 上级厂商id |
| name | string | 名称 |
| orderNum | string | 排序 |
| linkman | string | 联系人 |
| tel | string | 联系电话 |
| address | string | 联系地址 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "resquestId": "123454",
    "result": [{
        "address": "西斗门",
        "linkman": "test",
        "name": "中天",
        "orderNum": "1",
        "orgId": "113",
        "parentId": "1",
        "tel": "18812561389"
    }],
    "success": true,
    "totalCount": 100
}
```

2、禁用厂商

```
/disable
```

请求参数示例：

```
{"orgId":"223434"}
```



