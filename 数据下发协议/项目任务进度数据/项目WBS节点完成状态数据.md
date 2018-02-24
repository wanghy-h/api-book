### 项目WBS节点完成状态数据

* **接口说明**

发布已完成的WBS节点信息

* **接口地址**

 /progress/wbs-completion-status?token=***&start=12345&limit=200?projectId=10001

* **接口类型**

 Http

* **请求方式**

 GET

* **内容类型**

  application/json

* **请求参数**

| 参数名称 | 说明          |
| :-------| :------------ |
| token   | 权限标识       |
| start   | 本次请求所要获取的增量数据的tag起始值，客户端需要缓存接口返回的数据集合中最后一条数据的version值 |
| limit   | 返回指定的数据条数 上限为200条  0 < limit <= 200 |
| projectId   | 项目ID |

* **响应报文**

```json

[
    {
        "id": 324324,
        "wbsId": "12312312",
        "name": "北京xx工程咨询监理有限公司",
        "inputUserId": "2323",
        "inputUserName": "xcxxx",
        "actualEndTime": "2017-12-09 12:38:20",
        "createTime": "2017-12-09 12:38:20",
        "updateTime": "2017-12-09 12:38:20",
        "version": 2323232323,
        "deleted": false
    }
]

```

* **响应状态码**

| 字段名称 | 数据类型 |
| :--- | :--- |
| 200 | 成功 |
| 403 | token过期，请重新申请Token |
| 500 | 非法参数或接口执行异常 |

* **响应数据结构**

| 字段名称 | 字段类型 | 字段描述 |
| :--- | :--- | :--- |
| id | int | 数据唯一标识 |
| wbsId | string | wbs节点标识 |
| name | string | wbs节点名称 |
| inputUserId | string | 填报人ID |
| inputUserName | string | 填报人姓名 |
| actualEndTime | string | 实际结束时间 |
| createTime | date | 数据创建时间 |
| updateTime | date | 数据更新时间 |
| version | long | 当前数据版本 |
| deleted     | int  | 是否逻辑删除 **见表1**|

**表1**  是否逻辑删除标识

| deleted |  |
| :--- | :--- |
| false | 未删除 |
| true | 已删除 |
