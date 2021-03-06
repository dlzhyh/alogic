# /component/dbcp/List

## 概述

查询当前活跃dbcp列表。

服务的路径如下：
```
/component/dbcp/List
```

## 输入参数
无

## 输入文档
无

## 输出文档

输出为JSON文档，信息如下：

| 编号 | 代码 | 类型 | 名称 | 说明 |
| ---- | ---- | ---- | ---- | ---- |
| 1 | pool | Object [] | dbcp列表 | |

具体的pool对象定义见[/component/dbcp/Query](Query.md).

## 异常
* 如果调用成功，返回代码为core.ok;

## 样例

下面是一个样例，
服务地址如下；
```
http://localhost:9000/services/component/dbcp/List
```
输出结果：
```
	{
	    "duration": "23", 
	    "host": "0:0:0:0:0:0:0:1:9000", 
	    "reason": "It is successful", 
	    "pool": [
	        {
	            "maxActive": 30, 
	            "id": "itportal", 
	            "maxIdle": 5, 
	            "username": "itportal", 
	            "callbackId": "", 
	            "callback": "", 
	            "maxWait": 10000, 
	            "runtime": {
	                "pool": {
	                    "maxActive": 30, 
	                    "maxIdle": 5, 
	                    "creating": 0, 
	                    "idle": 1, 
	                    "wait": 0, 
	                    "working": 0
	                }, 
	                "stat": {
	                    "total": {
	                        "min": "429", 
	                        "max": "659", 
	                        "error": "0", 
	                        "times": "2", 
	                        "avg": "544.00"
	                    }, 
	                    "module": "com.logicbus.dbcp.util.ConnectionPoolStat", 
	                    "start": "20150910161259", 
	                    "current": {
	                        "min": "429", 
	                        "max": "659", 
	                        "error": "0", 
	                        "times": "2", 
	                        "avg": "544.00"
	                    }, 
	                    "lastVistiedTime": "20150910161354", 
	                    "cycleStart": "20150910161259"
	                }
	            }, 
	            "coder": "DES3", 
	            "driver": "org.mariadb.jdbc.Driver", 
	            "timeout": 3600, 
	            "url": "jdbc:mariadb://10.142.90.57:8088/itportal"
	        }
	    ], 
	    "code": "core.ok", 
	    "serial": "1441876396461vnTRip4"
	}
```


