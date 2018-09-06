## 分页查询返回报文结构：

| 字段 | 类型 | 说明 |
| :--- | :--- | :--- |
| success | bool | 是否成功 |
| code | int | 错误编码 |
| message | string | 错误描述 |
| requestId | string | 请求id，请求唯一标识 |
| result | Object | 查询返回的实体列表 |
| totalCount | int | 当前条件下查询到的总记录 |

## 分页查询其余业务返回报文结构：

| 字段 | 类型 | 说明 |
| :--- | :--- | :--- |
| success | bool | 是否成功 |
| code | int | 错误编码 |
| message | string | 错误描述 |
| requestId | string |  |
| result | Object | 业务处理返回实体 |

请求日期字符串格式：

| yyyy-mm-dd |
| :--- |


响应日期字符串格式：

| yyyy-mm-dd hh24:mi:ss |
| :--- |


所有接口请求方式均为`post`

页面下拉列表通用接口说明：

`使用字典管理如下接口查询列表 /api/base/dict/dictList`

各个下拉列表type定义如下：

```java
        /**
         * 菜单类型
         */
        String MENU_TYPE = "MenuType";
        /**
         * 删除标志
         */
        String DEL_FLAG = "DelFlag";
        /**
         *用户类型
         */
        String USER_TYPE = "UserType";
        /**
         * 用户状态
         */
        String USER_STATUS = "UserStatus";
        /**
         * 通讯方式
         */
        String NETWORK = "network";
        /**
         * 接入平台
         */
        String PLATFORM = "platform";
        /**
         * 数据类型
         */
        String DATA_TYPE = "dataType";
        /**
         * 产品状态
         */
        String PRODUCT_TYPE = "ProdType";
        /**
         * 设备状态
         */
        String DEVICE_STATUS = "devStatus";
```



