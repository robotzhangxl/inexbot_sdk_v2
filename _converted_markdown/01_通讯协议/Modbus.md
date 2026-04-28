# Modbus

Modbus 主站/从站通讯协议配置。

---

## 上位机设置 Modbus 主站参数

**命令字：** `0x7300`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| processNumber | int | 是 | 工艺号，范围 [1, 9] |
| type | string | 是 | 主站类型：`TCP` 或 `RTU` |
| masterStation | object | 是 | 主站参数 |

#### masterStation.RTU 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| baudrate | int | 波特率 |
| checkBit | string | 校验位：`N`、`E`、`O` |
| dataBit | int | 数据位，范围 [5, 8] |
| port | int | 端口号 |
| slaveId | int | 从站 ID，范围 [0, 65535] |
| stopBit | int | 停止位，`0` 或 `1` |

#### masterStation.TCP 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| IP | string | IP 地址 |
| endian_type | int | Float 大小端：`0`=AB CD，`1`=CD AB，`2`=BA DC，`3`=DC BA |
| port | int | 端口号，范围 [0, 65535] |

#### 其他参数

| 参数 | 类型 | 说明 |
|------|------|------|
| startAddress | bool | 地址偏移：`true`=地址不变，`false`=地址自动-1 |

### 请求示例

```json
{
  "processNumber": 1,
  "type": "TCP",
  "masterStation": {
    "TCP": {
      "IP": "192.168.1.14",
      "endian_type": 1,
      "port": 503
    },
    "RTU": {
      "baudrate": 115200,
      "checkBit": "E",
      "dataBit": 5,
      "port": 2,
      "slaveId": 1,
      "stopBit": 1
    }
  },
  "startAddress": false
}
```

---

## 上位机查询 Modbus 主站参数

**命令字：** `0x7301`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| processNumber | int | 是 | 工艺号，范围 [1, 9] |

### 请求示例

```json
{
  "processNumber": 1
}
```

### 响应参数

| 参数 | 类型 | 说明 |
|------|------|------|
| type | string | 主站类型 |
| modbus_state | bool | 连接状态：`true`=已连接，`false`=未连接 |
| response_time_out | int | 读写响应时间（ms） |

> 其他参数同设置请求

### 响应示例

```json
{
  "processNumber": 1,
  "type": "TCP",
  "masterStation": {
    "TCP": {
      "IP": "192.168.1.14",
      "endian_type": 1,
      "port": 503
    },
    "RTU": {
      "baudrate": 115200,
      "checkBit": "E",
      "dataBit": 5,
      "port": 2,
      "slaveId": 1,
      "stopBit": 1
    }
  },
  "modbus_state": false,
  "response_time_out": 100,
  "startAddress": false
}
```

---

## 上位机查询 Modbus 连接状态

**命令字：** `0x7303`

### 响应参数

| 参数 | 类型 | 说明 |
|------|------|------|
| ModbusConnect | bool | `true`=已连接，`false`=未连接 |

### 响应示例

```json
{
  "ModbusConnect": false
}
```

---

## 上位机设置 Modbus 从站参数

**命令字：** `0x7305`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| type | string | 是 | 通讯方式：`TCP` 或 `RTU` |
| master-slave | int | 是 | 主从模式：`0`=主站，`1`=从站 |
| scancycle | int | 否 | 扫描周期（ms），范围 [8, 1000] |
| stoprun | int | 否 | 通讯断开时操作：`0`=不停机，`1`=停机 |
| RTU | object | 否 | RTU 参数 |
| TCP | object | 否 | TCP 参数 |

#### RTU 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| baudrate | int | 波特率 |
| port | int | 端口号 |
| slaveId | int | 从站 ID，范围 [0, 65535] |

#### TCP 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| IP | string | IP 地址，默认值 `192.168.1.11` |
| endian_type | int | Float 大小端：`0`=AB CD，`1`=CD AB，`2`=BA DC，`3`=DC BA |
| port | int | 端口号，范围 [0, 65535] |

### 请求示例

```json
{
  "type": "TCP",
  "master-slave": 1,
  "scancycle": 100,
  "stoprun": 0,
  "RTU": {
    "baudrate": 115200,
    "port": 2,
    "slaveId": 1
  },
  "TCP": {
    "IP": "192.168.1.11",
    "endian_type": 0,
    "port": 502
  }
}
```

---

## 上位机设置从站连接使能

**命令字：** `0x7308`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| enable | bool | 是 | 连接使能 |

### 请求示例

```json
{
  "enable": true
}
```

---

## 上位机设置心跳检测使能

**命令字：** `0x7309`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| checkheart | bool | 是 | 心跳检测使能 |

### 请求示例

```json
{
  "checkheart": true
}
```

---

## 上位机查询心跳检测使能

**命令字：** `0x703A`

### 响应参数

| 参数 | 类型 | 说明 |
|------|------|------|
| checkheart | bool | 心跳检测使能状态 |

---

## 上位机设置 Modbus 程序

**命令字：** `0x703C`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| robot | int | 是 | 当前机器人号 |
| programid | int | 是 | 程序序号，范围 [1, 300] |
| jobname | string | 是 | 已选程序名称 |

### 请求示例

```json
{
  "robot": 1,
  "programid": 1,
  "jobname": "AA"
}
```

---

## 上位机查询 Modbus 程序

**命令字：** `0x703D`

### 请求参数

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| robot | int | 是 | 当前机器人号 |
| num | int | 是 | 查询数量，固定为 10 |
| startprogramid | int | 是 | 查询序列起始程序序号，范围 [1, 30] |

### 请求示例

```json
{
  "robot": 1,
  "num": 10,
  "startprogramid": 1
}
```

### 响应参数

| 参数 | 类型 | 说明 |
|------|------|------|
| robot | int | 当前机器人号 |
| jobnamelist | string[] | 程序名称列表，长度为 10 |
| startprogramid | int | 序列起始程序序号 |
| sum | int | 可选程序总数 |
