# Tcp通讯

本文档介绍上位机与控制器之间的 TCP 通讯配置与使用。

---

## 上位机设置 Tcp 通讯参数

**命令字：** `0x7320`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| type | int | 是 | TCP 通讯方式：`0`=服务器，`1`=客户端，`2`=配置文件 |
| robot | int | 是 | 当前机器人号，范围 [1, 4] |
| craft | int | 是 | 工艺号，范围 [1, 9] |
| client | object | 否 | 客户端参数（当 `type=1` 时存在） |
| server | object | 否 | 服务器参数（当 `type=0` 时存在） |

#### client 对象

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| ip | string | 是 | 需要连接的服务器 IP |
| port | int | 是 | 通讯端口，范围 (0, 65535] |
| frameHeader | string | 否 | 数据帧头，留空表示没有 |
| terminator | string | 否 | 数据帧尾，留空表示没有 |
| separator | string | 否 | 数据分隔符 |
| numberSystem | int | 否 | 接收数据的进制：`0`=十进制，`1`=十六进制 |

#### server 对象

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| ip | string | 是 | 当前用作服务器 IP |
| port | int | 是 | 通讯端口，范围 (0, 65535] |
| frameHeader | string | 否 | 数据帧头，留空表示没有 |
| terminator | string | 否 | 数据帧尾，留空表示没有 |
| separator | string | 否 | 数据分隔符 |
| numberSystem | int | 否 | 接收数据的进制：`0`=十进制，`1`=十六进制 |

### 请求示例

```json
{
  "type": 1,
  "craft": 1,
  "robot": 1,
  "client": {
    "frameHeader": "@",
    "ip": "192.168.1.111",
    "numberSystem": 0,
    "port": 9000,
    "separator": ",",
    "terminator": "!"
  },
  "server": {
    "frameHeader": "@",
    "ip": "192.168.0.229",
    "numberSystem": 0,
    "port": 9001,
    "separator": ",",
    "terminator": "!"
  }
}
```

---

## 上位机查询 Tcp 通讯参数

**命令字：** `0x7321`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| type | int | 是 | `0`=服务器参数，`1`=客户端参数，`2`=配置文件 |
| robot | int | 是 | 机器人号，范围 [1, 4] |
| craft | int | 是 | 工艺号，范围 [1, 9] |

> **注意：** `type=2` 时控制器发送服务器参数

### 请求示例

```json
{
  "craft": 1,
  "robot": 1,
  "type": 2
}
```

### 响应参数

| 参数 | 类型 | 说明 |
|------|------|------|
| type | int | TCP 通讯方式 |
| robot | int | 当前机器人号 |
| craft | int | 当前工艺号 |
| client | object | 客户端参数（当 `type=1` 时存在） |
| server | object | 服务器参数（当 `type=0` 时存在） |

### 响应示例

```json
{
  "type": 1,
  "craft": 1,
  "robot": 1,
  "client": {
    "frameHeader": "@",
    "ip": "192.168.1.111",
    "numberSystem": 0,
    "port": 9000,
    "separator": ",",
    "terminator": "!"
  },
  "server": {
    "frameHeader": "@",
    "ip": "192.168.0.229",
    "numberSystem": 0,
    "port": 9001,
    "separator": ",",
    "terminator": "!"
  }
}
```

---

## 上位机请求连接 Tcp 通讯

**命令字：** `0x7323`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| robot | int | 是 | 当前机器人号，范围 [1, 4] |
| craft | int | 是 | 工艺号，范围 [1, 9] |

### 请求示例

```json
{
  "craft": 1,
  "robot": 1
}
```

---

## 上位机请求断开 Tcp 通讯

**命令字：** `0x7324`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| robot | int | 是 | 当前机器人号，范围 [1, 4] |
| craft | int | 是 | 工艺号，范围 [1, 9] |

### 请求示例

```json
{
  "craft": 1,
  "robot": 1
}
```
