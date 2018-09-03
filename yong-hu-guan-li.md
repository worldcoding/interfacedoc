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



