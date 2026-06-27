# 1.MCP能干什么

## 程序员使用

开发部署项目，
写SQL语句
manus智能体

## 大众使用

旅游规划

## 联网搜索

# 2.MCP是什么

Model Context Protocol（模型上下文协议），是一个开放的协议标准，定义了AI模型与外部工具、数据源、服务等进行交互的方式和规范。通过MCP，AI模型可以访问和利用各种外部资源，增强其功能和应用场景。

## 哪些平台支持MCP查询

Smithery平台

# 3.程序员如何使用MCP

## MCP通信机制

- stdio：标准输入输出流，适用于简单的交互场景。
    - 优点
        - 适合客户端和服务端在同一台机器上运行的场景，简单
        - stdio模式无需外部网络依赖，通信速度快，适合快速响应的本地应用
        - 可靠性高，且易于调试
    - 缺点
        - stdio的配置比较负载
        - stdio模式为单进程通信，无法并行处理多个客户端请求，同时由于进程资源开销较大，不适合在本地运行大量服务
- sse：Server-Sent Events，适用于实时数据推送和事件通知。
    - 优点
        - 配置简单，适合实时数据推送和事件通知
        - 适合浏览器端的应用，支持跨域请求

## stdio的本地环境

一种是python编写的服务，一种是TypeScript编写的服务
分别对应着uvx和npx两种指令

uvx安装方式：pip install uvx

mcp mysql server（github上找下 https://github.com/burakdirin/mysqldb-mcp-server）

# 4.MCP的工作原理

MCP遵循客户端-服务器架构（client-server）,其中包含以下几个核心概念：

- MCP主机（MCP Hosts）例如Claude,code
- MCP客户端（MCP Clients）,充当LLM和MCP server之间的桥梁，嵌入在主机程序中；
    - 接收来自LLM的请求，
    - 并将其转发给MCP server
    - 接收MCP server的响应，并将其返回给LLM
- MCP服务器（MCP Servers），既可以是本地的（stdio的方式），也可以是远程的（sse的方式），负责处理来自MCP客户端的请求，并与外部资源进行交互。
- 本地资源（Local Resources）例如数据库，本地文件
- 远程资源（Remote Resources）例如高德地图

## MCP工作流程

API主要有两个

- tool/list: 列出Server支持的所有工具
- tools/call:Client请求Server去执行某个工具，并将结果返回

# 5.手动开发MCP项目（C/S）

# 6.大众用户如何使用MCP

# 7.热门MCP Servers推荐

# 8.A2A协议：开启Agent间协作



