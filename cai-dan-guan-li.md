## 菜单管理

```
/api/base/menu
```

1、获取所有菜单

```
/list
```

无请求参数

返回报文示例：

```
{
    "result": [{
        "meunId": "432",
        "parentId": "123",
        "name": "系统管理"
    }],
    "requestId": "233334",
    "code": 0,
    "message": "成功",
    "success": true
}
```

2、菜单分页列表

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
| parentId |  |  |
| menuId |  |  |
| name |  |  |
| url |  |  |
| type |  |  |
| icon |  |  |
| perms |  |  |
| orderNum |  |  |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "icon": "url",
        "meunId": "1",
        "name": "系统管理",
        "parentId": "0",
        "perms": "insert.user",
        "type": "1",
        "url": "url"
    }],
    "success": true,
    "totalCount": 100
}
```



