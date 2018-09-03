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

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "success": true
}
```

3、厂商详情

```
/detail
```

请求参数示例：

```
{"orgId":"223434"}
```

返回报文参数：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| name | string | 厂商名称 |
| linkman | string | 联系人 |
| tel | string | 联系电话 |
| address | string | 地址 |
| gmtCreate | date | 注册时间 |
| gmtModified | date | 更新时间 |
| userList | array | 厂商用户列表 |
| userList.userId | string | 用户id |
| userList.name | string | 用户名 |
| userList.nick | string | 昵称 |
| userList.mobile | string | 电话 |
| userList.gmtCreate | date | 添加时间 |
| userList.role | string | 用户角色 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "resquestId": "1989999",
    "result": {
        "address": "西斗门路",
        "linkman": "test",
        "name": "中天",
        "tel": "13834535345",
        "userList": [{
            "email": "324453@qq.com",
            "mobile": "18812561389",
            "name": "test",
            "nick": "hello",
            "role": "客服",
            "userId": 1324
        }]
    },
    "success": true
}
```

3、修改厂商

```
/modify
```

请求参数示例：

```
{
    "address": "西斗门",
    "linkman": "test",
    "name": "中天",
    "orgId": "113",
    "tel": "18812561389"
}
```



