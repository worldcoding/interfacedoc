## 用户管理

```
/api/base/user
```

1、用户登录

```
/login
```

请求参数示例：

```
{
    "name": "用户名",
    "password": "密码"
}
```

返回报文示例：

```
{
    "result":{"Authorization","token"},
    "requestId":"233334",
    "code": 0,
    "message": "成功",
    "success": true
}
```

2、查询当前厂商的所有用户

```
/orgUserList
```

请求参数示例：

```
{"userId":"223434"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "1989999",
    "result": [{
        "email": "324453@qq.com",
        "mobile": "18812561389",
        "name": "test",
        "roleList": [{
            "roleId": "123",
            "name": "客服"
        }],
        "nick": "hello"
    }],
    "success": true
}
```

3、重置密码

```
/resetPwd
```

请求参数示例：

```
{"userId":"223434"}
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

4、删除用户

```
/delete
```

请求参数示例：

```
{"userId":"223434"}
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

5、厂商注册

```
/addOrg
```

请求参数：

| 字段 | 类型 | 名称 | 说明 |
| :--- | :--- | :--- | :--- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |



