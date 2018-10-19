# 角色管理

```
/api/base/role
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
    "pageIndex": 1,
    "pageSize": 10
}
```

返回实体结构：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| roleId | string | 角色id |
| name | string | 角色名称 |
| roleType | int | 类型 |
| roleTypeName | string | 类型描述 |
| remark | string | 角色说明 |
| gmtCreate | string | 创建时间 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "gmtCreate": "2018-09-04 09:48:21",
        "remark": "备注",
        "roleId": "100001",
        "roleName": "系统管理员",
        "roleType": "0",
        "roleType": "厂商用户角色"
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
| roleType | int | 类型 |  |
| remark | string | 备注 |  |
| funList | array | 角色权限列表 |  |

请求参数示例：

```
{
    "funList": ["1244"],
    "roleType": "0"
    "name": "管理员",
    "remark": "备注"
}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId":"233334",
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

返回报文同新增

4、删除角色

```
/delete
```

请求参数示例：

```
{"roleId":"223434"}
```

5、角色详情

```
/detail
```

请求参数示例：

```
{"roleId":"223434"}
```

返回报文：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| name | string | 角色名称 |
| remark | string | 备注 |
| menuList | array | 菜单列表 |
| menuList.parentId | string | 上级菜单id |
| menuList.menuId | string | 菜单id |
| menuList.name | string | 菜单名称 |
| menuList.select | bool | 是否拥有此菜单权限 |

返回报文示例：

```
{
    "menuList": [{
        "meunId": "1223",
        "name": "test",
        "parentId": "0",
        "select": true
    }],
    "name": "管理员",
    "remark": "备注"
}
```

6、角色列表

```
/list
```

请求参数：

```
{"roleType":1}
```

返回报文：

```
{
    "code": 0,
    "message": "成功",
    "requestId":"233334",
    "success": true,
    "result": {"roleId":"333","roleName":"开发人员"}
}
```



