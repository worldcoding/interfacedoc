# 角色管理

```
/api/base/sysRole
```

1、角色分页列表

```
/pageList
```

请求参数：

| 字段 | 类型 | 名称 | 说明 |
| :--- | :--- | :--- | :--- |
| pageIndex | int | 页面索引 | 大于0的数字 |
| pageSize | int | 分页大小 | 大于0的数字 |
| name | string | 角色名称 | 可为空 |

请求参数示例：

```
{
    "name": "管理员",
    "pageIndex": "1",
    "pageSize": "10"
}
```

返回实体结构：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| roleId | string | 角色id |
| name | string | 角色名称 |
| remark | string | 角色说明 |
| gmtCreate | Date | 创建时间 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "resquestId": "123454",
    "result": [{
        "gmtCreate": 1535955721965,
        "remark": "备注",
        "roleId": "100001",
        "roleName": "系统管理员"
    }],
    "success": true,
    "totalCount": 100
}
```

2、新增角色

```
/add
```

请求参数：

| 字段 | 类型 | 名称 | 说明 |
| :--- | :--- | :--- | :--- |
| name | string | 角色名称 |  |
| remark | string | 备注 |  |
| funList | array | 角色权限列表 |  |

请求参数示例：

```
{
    "funList": ["1244"],
    "name": "管理员",
    "remark": "备注"
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

3、修改角色

```
/modify
```

请求参数：

| 字段 | 类型 | 名称 | 说明 |
| :--- | :--- | :--- | :--- |
| roleId | string | 角色id |  |
| name | string |  |  |
| remark | string |  |  |
| funList | array |  |  |

请求参数示例：

```
{
    "roleId": "123466"
    "funList": ["1244"],
    "name": "管理员",
    "remark": "备注"
}
```



