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
{"orgId":"223434"}
```

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "1989999",
    "result": [{
        "userId": "22233",
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
| name | string | 厂商名称 |  |
| linkman | string | 联系人 |  |
| tel | string | 联系电话 |  |
| address | string | 地址 |  |
| userName | string | 用户名 |  |
| password | string | 密码 |  |

请求参数示例：

```
{
    "address": "西斗门",
    "linkman": "张三",
    "name": "中天微",
    "password": "123456",
    "tel": "13812561389",
    "userName": "hello"
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

6、修改密码

```
/modifyPwd
```

请求参数示例：

```
{"oldPwd:"123","newPwd":"556"}
```

7、获取当前厂商下所有普通用户

```
/pageList
```

请求参数示例：

```
{
    "name": "hello",
    "pageIndex": 1,
    "pageSize": 10
}
```

返回报文实体：

| 字段 | 类型 | 名称 |
| :--- | :--- | :--- |
| name | string | 用户名 |
| nick | string | 昵称 |
| email | string | 邮箱 |
| mobile | string | 手机 |
| gmtCreate | string | 创建时间 |
| orgName | string | 所属厂商 |
| deviceNum | string | 设备数量 |
| status | string | 状态 |

返回报文示例：

```
{
    "code": 0,
    "message": "成功",
    "requestId": "123454",
    "result": [{
        "deviceNum": "3",
        "email": "2222222@qq.com",
        "gmtCreate": '2018-09-06 19:08',
        "mobile": "122334455",
        "orgName": "中天",
        "status": "正常"
    }],
    "success": true,
    "totalCount": 100
}
```

8、禁用用户

```
/disable
```

请求参数示例：

```
{"userId","12343"}
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

9、厂商用户信息修改

```
/modifyOrgUser
```



