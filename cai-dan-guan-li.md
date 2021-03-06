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
| parentId | string |  |
| menuId | string |  |
| name | string |  |
| url | string |  |
| type | string |  |
| typeName | string | 类型对应名称 |
| icon | string |  |
| perms | string |  |
| orderNum | string |  |

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
        "typeName":"目录",
        "url": "url",
        "orderNum":"1"
    }],
    "success": true,
    "totalCount": 100
}
```

3、新增菜单

```
/add
```

请求参数：

| 字段 | 类型 | 名称 | 说明 |
| :--- | :--- | :--- | :--- |
| name | string | 菜单名称 |  |
| parentId | string | 上级菜单Id |  |
| type | string | 菜单类型 | 0:目录,1:菜单,2:按钮 |
| icon | string | 图标url |  |
| perms | string | 授权标识 |  |
| orderNum | string | 排序数值 |  |
| url | string | 菜单url |  |

请求参数示例：

```
{
    "icon": "url",
    "name": "系统管理",
    "parentId": "0",
    "perms": "insert.user",
    "type": "1",
    "url": "url",
    "orderNum":"2"
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

4、修改菜单

```
/modify
```

请求参数说明同新增

请求参数示例：

```
{
    "menuId": "234",
    "icon": "url",
    "name": "系统管理",
    "parentId": "0",
    "perms": "insert.user",
    "type": "1",
    "url": "url",
    "orderNum":"2"
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

5、删除菜单

```
/delete
```

请求参数示例：

```
{"menuId":"12333"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "success": true
}
```

6、获取用户所有菜单（侧边栏）

```
/userMenuList
```

无请求参数

返回报文示例：

```
{
    "result": [{
    "name": "系统管理",
    "icon": "",
    "menuId": "1000",
    "type": "0",
    "parentId": "0",
    "url": "/systemControl",
    "children": [{
        "children": [],
        "name": "系统日志",
        "icon": "",
        "menuId": "1021",
        "type": "1",
        "parentId": "1000",
        "url": "/systemControl/logManage"
    }]
}],
    "requestId": "233334",
    "code": 0,
    "message": "成功",
    "success": true
}
```

7、获取当前用户的操作权限

```
/menuPermsList
```

无请求参数

返回报文示例：

```
{
    "result": ["sys.module.list", "sys.prodType.info", "sys.role.update", "sys.role.info", 
    "sys.role.delete", "sys.dict.add", "sys.org.disable"],
    "requestId": "233334",
    "code": 0,
    "message": "成功",
    "success": true
}
```



