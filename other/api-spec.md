## [example] - 接口文档示例说明
- AUTH
```
# 是否需要鉴权
auth_req = true 

# 鉴权的方式为token
auth_method = [header] auth-token 

# 鉴权的方式为key
auth_method = [header] secret-id/secret-key 
```
- PATH
```
# 接口的请求路径
/example/echo
```
- METHOD
```
# 接口支持的方法
POST/GET
```
- PARAMETER
```
# 接口支持的入参 [参数名称] - [是否必填], [数据类型(长度限制)], [默认值], [补充描述]
request_id - [optional], [string(255)], like echo, server will return what you sent. 
limit - [optional], [int], [default 10], the amount of items for pagination. 
offset - [optional], [int], [default 0], for pagination usage. 
```
- REQUEST EXAMPLE
```
# 请求示范
POST /example/echo
{"limit":10,"offset":0,"request_id":"echo_this_id"}
```
- RESPONCE EXAMPLE
```
# 响应示范
{
  "request_id": "echo_this_id",
  "error_code": 0,
  "error_msg": "",
  "timestamp": 1665494133,
  "data": {
    "params": {
      "1": "dev",
      "2": "request",
      "3": "parse"
    },
    "auth": [],
    "data": {
      "get": [],
      "post": "{\"limit\":10,\"offset\":0,\"request_id\":\"echo_this\"}",
      "header": {
        "Host": "devtest1.sideai.com",
        "Connection": "keep-alive",
        "Content-Length": "48",
        ..."
      }
    }
  }
}
```