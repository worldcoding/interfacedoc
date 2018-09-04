## 系统日志

```
/api/base/log
```

1、日志分页列表

```
/sysPageList
```

请求参数：

| 字段 | 类型 | 名称 | 说明 |
| :--- | :--- | :--- | :--- |
| pageIndex | int |  |  |
| pageSize | int |  |  |
| condition | Object | 检索条件 |  |
| condition.name | string | 用户名 |  |
| condition.beginDate | string | 日志创建开始时间 | 格式：2018-09-04 |
| conditon.endDate | string | 日志创建结束时间 |  |

请求参数示例：

```
{
    "condition": {
        "name": "hello",
        "beginDate": "2018-09-04",
        "endDate": "2018-0904"
    },
    "pageIndex": 1,
    "pageSize": 10
}
```



