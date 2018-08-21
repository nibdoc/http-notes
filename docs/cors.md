# CORS - 跨站资源共享

CORS(Cross Origin resource shared, 跨站资源共享)

跨域时触发改机制

## 简单请求与预检请求

满足以下全部条件即为简单请求：

- HTTP方法
    - GET
    - HEAD
    - POST

- 请求首部只包含以下安全首部
    - Accept
    - Accept-Language
    - Content-Language
    - Content-Type

- Content-Type只为以下值
    - text/plain
    - multipart/form-data
    - application/x-www-form-urlencoded

- XMLHttpRequestUpload未注册事件。

- 没有ReadableStream对象。

以上条件有一条不满足即为预检请求，需要发送OPTIONS请求。

## 响应头

- Access-Control-Allow-Origin

- Access-Control-Allow-Headers

- Access-Control-Allow-Methods

- Access-Control-Max-Age

- Access-Control-Allow-Credentials: true

    客户端同样需要设置对应的发送标志位