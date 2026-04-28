# OPC UA

OPC UA 协议配置，支持客户端和服务器两种模式。

---

## 上位机设置 OPC UA 参数

**命令字：** `0x7350`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| client | object | 否 | 客户端参数 |
| server | object | 否 | 服务器参数 |

#### client 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| enable | bool | 连接使能 |
| ip | string | 服务器 IP 地址 |
| port | int | 端口号，范围 [0, 65535] |
| resource | string | 服务器名称 |

#### server 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| enable | bool | 连接使能 |
| ip | string | 控制器作为服务器时的 IP 地址 |
| port | int | 端口号，范围 [0, 65535] |

### 请求示例

```json
{
  "client": {
    "enable": false,
    "ip": "192.168.1.240",
    "port": 49400,
    "resource": "ProsysServer"
  },
  "server": {
    "enable": false,
    "ip": "192.168.0.229",
    "port": 4840
  }
}
```

---

## 上位机查询 OPC UA 参数

**命令字：** `0x7351`

> 无需请求参数

**响应：** 同 `0x7350` 格式
