---
title: DH参数
source: DH参数.docx
category: 运动控制
---

# DH参数

## 机器人基础参数

> 说明：包含DH参数、关节参数、笛卡尔参数等机器人基础参数的设置与查询


---

## 上位机设置当前机器人DH参数

**命令字: 0x20C0**


### 六轴串联机器人（存在耦合时动态限位生效）

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "fiveAxisDirection" | double | 五轴方向；double类型，范围0,90 度 |
| "dynamicLimit" | string | J2+J3范围限制 |
| "max" | double | J2+J3最大值；double类型，范围[-500,500] |
| "min" | double | J2+J3最小值；double类型，范围[-500,500] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":0.0,
"L8":0.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"dynamicLimit":
{
"max":0.0,
"min":0.0
},
"fiveAxisDirection":90.0,
"mountAngle":false,
"robot":1
}
```

### 六轴协作机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "threeAxisDirection" | double | 三轴方向；double类型，范围-90,0 度 |
| "fiveAxisDirection" | double | 五轴方向；double类型，范围0,90 度 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"fiveAxisDirection":90.0,
"mountAngle":false,
"robot":1,
"threeAxisDirection":-90.0
}
```

### 六轴喷涂机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L7杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":0.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":0.0,
"L8":0.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"mountAngle":false,
"robot":1
}
```

### 六轴异型二

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"mountAngle":false,
"robot":1
}
```

### 五轴串联多关节

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "fiveAxisDirection" | double | 五轴方向；double类型，范围0,90 度 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":0.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"fiveAxisDirection":90.0,
"mountAngle":false,
"robot":1
}
```

### 四轴SCARA

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio34":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1
}
```

### 四轴SCARA异型1

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"couplingRatio34":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1
}
```

### 四轴连杆码垛

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | 偏置值；double类型，范围[-4000,4000]；默认为0 |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "maxDynamicLimit" | double | J2+J3最大值；double类型，范围[-1000,1000] |
| "minDynamicLimit" | double | J2+J3最小值；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":0.0,
"couplingRatio23":0.0,
"couplingRatio34":0.0,
"maxDynamicLimit":0.0,
"minDynamicLimit":0.0,
"mountAngle":false,
"robot":1
}
```

### 四轴码垛丝杆

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "amplificationRatio" | double | 放大比；double类型，范围[1,1000] |
| "conversionRatio2" | double | 二轴转换比；double类型，范围[1,1000] |
| "conversionRatio3" | double | 三轴转换比；double类型，范围[1,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"amplificationRatio":100.0,
"conversionRatio2":100.0,
"conversionRatio3":100.0,
"mountAngle":false,
"robot":1
}
```

### 四轴串联多关节

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"couplingRatio23":0.0,
"couplingRatio34":0.0,
"mountAngle":false,
"robot":1
}
```

### 四轴直角机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"conversionRatio_X":100.0,
"conversionRatio_Y":100.0,
"conversionRatio_Z":100.0,
"mountAngle":false,
"robot":1
}
```

### 四轴极坐标异型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "conversionRatio2" | double | 二轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio3" | double | 三轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"conversionRatio2":100.0,
"conversionRatio3":100.0,
"mountAngle":false,
"robot":1
}
```

### 三轴SCARA

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1
}
```

### 三轴直角机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"conversionRatio_X":100.0,
"conversionRatio_Y":100.0,
"conversionRatio_Z":100.0,
"mountAngle":false,
"robot":1
}
```

### 三轴直角异型1

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "conversionRatio2" | double | 二轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio3" | double | 三轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"conversionRatio2":100.0,
"conversionRatio3":100.0,
"mountAngle":false,
"robot":1
}
```

### 二轴SCARA

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L2":120.0,
"L3":120.0,
"mountAngle":false,
"robot":1
}
```

### 七轴串联多关节

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "Link" | string | DH参数列表 |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"Link":
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0
},
"mountAngle":false,
"robot":1
}
```

### 龙门焊接模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L4":120.0,
"L5":120.0,
"conversionRatio_X":100.0,
"conversionRatio_Y":100.0,
"conversionRatio_Z":100.0,
"mountAngle":false,
"robot":1
}
```

### 四轴并联机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000]；L2的值需要小于L3的值 |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":110.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"mountAngle":false,
"robot":1
}
```

### 酒槽机型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "L9" | double | L9杆长；double类型，范围[-4000,4000] |
| "L10" | double | L10杆长；double类型，范围[-4000,4000] |
| "L11" | double | L11杆长；double类型，范围[-4000,4000] |
| "L12" | double | 滑动电动缸导程；double类型，范围[-4000,4000] |
| "L13" | double | 顶升电动缸导程；double类型，范围[-4000,4000] |
| "L14" | double | 喷料距离；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"L8":120.0,
"L9":120.0,
"L10":120.0,
"L11":120.0,
"L12":120.0,
"L13":120.0,
"L14":120.0,
"mountAngle":false,
"robot":1
}
```

### 龙门焊接2模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L4":120.0,
"L5":120.0,
"conversionRatio_X":100.0,
"conversionRatio_Y":100.0,
"conversionRatio_Z":100.0,
"mountAngle":false,
"robot":1
}
```

### 四轴直角异型一

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "Link" | string | DH参数列表 |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "conversionRatio" | array | 轴转换比；double类型，范围[1,1000]；长度为2，第一个值为一轴转换比，第二个轴为四轴转换比 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"Link":
{
"L1":120.0,
"L2":120.0,
"conversionRatio":[100.0,100.0]
},
"mountAngle":false,
"robot":1
}
```

### 六轴龙门焊接模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "fiveAxisDirection" | double | 五轴方向；double类型，范围-90,0 度；0为五轴竖直向下，-90为五轴水平向右 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"conversionRatio_X":100.0,
"conversionRatio_Y":100.0,
"conversionRatio_Z":100.0,
"couplingRatio45":0.0,
"couplingRatio56":0.0,
"fiveAxisDirection":0.0,
"mountAngle":false,
"robot":1
}
```

### 五轴混动机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "L9" | double | L9杆长；double类型，范围[-4000,4000] |
| "L10" | double | L10杆长；double类型，范围[-4000,4000] |
| "conversionratio_J1" | double | 1轴转换比；double类型，范围[-4000,4000] |
| "conversionratio_J2" | double | 2轴转换比；double类型，范围[-4000,4000] |
| "conversionratio_J3" | double | 3轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"L8":120.0,
"L9":0.0,
"L10":120.0,
"conversionratio_J1":100.0,
"conversionratio_J2":100.0,
"conversionratio_J3":100.0,
"mountAngle":false,
"robot":1
}
```

### 四轴SCARA异型2

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | 1轴螺距；double类型，范围[-1000,0),(0,1000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 3轴螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":100.0,
"L2":120.0,
"L3":120.0,
"couplingRatio34":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1
}
```

### 六轴异型三

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "L9" | double | L9杆长；double类型，范围[-4000,4000] |
| "L10" | double | L10杆长；double类型，范围[-4000,4000] |
| "L11" | double | L11杆长；double类型，范围[-4000,4000] |
| "L12" | double | L12杆长；double类型，范围[-4000,4000] |
| "L13" | double | L13杆长；double类型，范围[-4000,4000] |
| "L14" | double | L14杆长；double类型，范围[-4000,4000] |
| "L15" | double | L15杆长；double类型，范围[-4000,4000] |
| "L16" | double | L16杆长；double类型，范围[-4000,4000] |
| "L17" | double | L17杆长；double类型，范围[-4000,4000] |
| "L18" | double | L18杆长；double类型，范围[-4000,4000] |
| "L19" | double | L19杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"L8":120.0,
"L9":120.0,
"L10":120.0,
"L11":120.0,
"L12":120.0,
"L13":120.0,
"L14":120.0,
"L15":120.0,
"L16":120.0,
"L17":120.0,
"L18":120.0,
"L19":120.0,
"mountAngle":false,
"robot":1
}
```

### 三轴SCARA异型一

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"mountAngle":false,
"robot":1
}
```

### delta2D并联机器人模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000]；L2的值需要小于L3的值 |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":110.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"mountAngle":false,
"robot":1
}
```

### 龙门焊接3模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "threeAxisDirection" | double | 四轴方向；double类型，范围0,90 度；四轴方向为0时，L4应填0 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L4":120.0,
"L5":120.0,
"conversionRatio_X":100.0,
"conversionRatio_Y":100.0,
"conversionRatio_Z":100.0,
"mountAngle":false,
"robot":1,
"threeAxisDirection":90.0
}
```

### 三轴串联异型一

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "threeAxisDirection" | double | 三轴方向；double类型，范围0,90 度 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"mountAngle":false,
"robot":1,
"threeAxisDirection":90.0
}
```

### 五轴协作机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000]；L2请填负值 |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000]；L6请填负值 |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":-120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":-120.0,
"L7":120.0,
"L8":120.0,
"mountAngle":false,
"robot":1
}
```

### 四轴SCARA异型3

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"couplingRatio12":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1
}
```

### 六轴串联-CBBARA

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000]；L2请填负值 |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":-120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":0.0,
"L7":0.0,
"L8":120.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"mountAngle":false,
"robot":1
}
```

### 高格立柱旋转四轴

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "conversionRatio1" | double | 1轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio2" | double | 3轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |

```json
{
"L1":120.0,
"L2":120.0,
"conversionRatio1":100.0,
"conversionRatio2":100.0,
"mountAngle":false,
"robot":1
}
```

---

## 上位机查询当前机器人DH参数

**命令字：0x20C1**


---

## 控制器回复上位机当前机器人DH参数

**命令字: 0x20C2**


### 六轴串联机器人（存在耦合时动态限位生效）

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "fiveAxisDirection" | double | 五轴方向；double类型，范围0,90 度 |
| "dynamicLimit" | string | J2+J3范围限制 |
| "max" | double | J2+J3最大值；double类型，范围[-500,500] |
| "min" | double | J2+J3最小值；double类型，范围[-500,500] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "angleToDistanceSync" | array | 机器人外部轴角度转距离列表；double类型；长度为当前机器人外部轴的总轴数，没有外部轴时该节点不存在；旋转轴值都为1，直线轴公式为：1 * 轴方向转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngleSync" | array | 机器人外部轴距离转角度列表；double类型；长度为当前机器人外部轴的总轴数，没有外部轴时该节点不存在；旋转轴值都为1，直线轴公式为：1 / 轴方向转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":0.0,
"L8":0.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"dynamicLimit":
{
"max":0.0,
"min":0.0
},
"fiveAxisDirection":90.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
"angleToDistanceSync":[27.775,27.775,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
"distanceToAngleSync":[0.03600360036,0.03600360036,1.0],
"robotType":1
}
```

### 六轴协作机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "threeAxisDirection" | double | 三轴方向；double类型，范围-90,0 度 |
| "fiveAxisDirection" | double | 五轴方向；double类型，范围0,90 度 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"fiveAxisDirection":90.0,
"mountAngle":false,
"robot":1,
"threeAxisDirection":-90.0,
"angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
"robotType":7
}
```

### 六轴喷涂机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L7杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":0.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":0.0,
"L8":0.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
"robotType":15
}
```

### 六轴异型二

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
"robotType":18
}
```

### 五轴串联多关节

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio32" | double | 3/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "fiveAxisDirection" | double | 五轴方向；double类型，范围0,90 度 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":0.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio32":0.0,
"couplingRatio34":0.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"fiveAxisDirection":90.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0,1.0],
"robotType":6
}
```

### 四轴SCARA

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第三位公式：1 * 螺距 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第三位公式：1 / 螺距 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"couplingRatio34":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1,
"angleToDistance":[1.0,1.0,0.222222222222,1.0],
"distanceToAngle":[1.0,1.0,4.5,1.0],
"robotType":2
}
```

### 四轴SCARA异型1

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * 螺距 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / 螺距 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"couplingRatio34":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1,
"angleToDistance":[0.222222222222,1.0,1.0,1.0],
"distanceToAngle":[4.5,1.0,1.0,1.0],
"robotType":13
}
```

### 四轴连杆码垛

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | 偏置值；double类型，范围[-4000,4000]；默认为0 |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "maxDynamicLimit" | double | J2+J3最大值；double类型，范围[-1000,1000] |
| "minDynamicLimit" | double | J2+J3最小值；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":0.0,
"couplingRatio23":0.0,
"couplingRatio34":0.0,
"maxDynamicLimit":0.0,
"minDynamicLimit":0.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0],
"robotType":3
}
```

### 四轴码垛丝杆

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "amplificationRatio" | double | 放大比；double类型，范围[1,1000] |
| "conversionRatio2" | double | 二轴转换比；double类型，范围[1,1000] |
| "conversionRatio3" | double | 三轴转换比；double类型，范围[1,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第二位公式：1 * 二轴转换比 / 360；第三位公式：1 * 三轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第二位公式：1 / 二轴转换比 * 360；第三位公式：1 / 三轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"amplificationRatio":100.0,
"conversionRatio2":100.0,
"conversionRatio3":100.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,0.277777777778,0.277777777778,1.0],
"distanceToAngle":[1.0,3.6,3.6,1.0],
"robotType":14
}
```

### 四轴串联多关节

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"couplingRatio23":0.0,
"couplingRatio34":0.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0],
"robotType":4
}
```

### 四轴直角机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * X轴转换比 / 360；第二位公式：1 * Y轴转换比 / 360；第三位公式：1 * Z轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / X轴转换比 * 360；第二位公式：1 / Y轴转换比 * 360；第三位公式：1 / Z轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"conversionRatio_X":100.0,
"conversionRatio_Y":100.0,
"conversionRatio_Z":100.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[0.277777777778,0.277777777778,0.277777777778,1.0],
"distanceToAngle":[3.6,3.6,3.6,1.0],
"robotType":16
}
```

### 四轴极坐标异型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "conversionRatio2" | double | 二轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio3" | double | 三轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第二位公式：1 * 二轴转换比 / 360；第三位公式：1 * 三轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第二位公式：1 / 二轴转换比 * 360；第三位公式：1 / 三轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"conversionRatio2":100.0,
"conversionRatio3":90.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,0.277777777778,0.25,1.0],
"distanceToAngle":[1.0,3.6,4.0,1.0],
"robotType":17
}
```

### 三轴SCARA

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "couplingRatio23" | double | 2/3耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第三位公式：1 * 螺距 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第三位公式：1 / 螺距 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"couplingRatio12":0.0,
"couplingRatio23":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1,
"angleToDistance":[1.0,1.0,0.222222222222],
"distanceToAngle":[1.0,1.0,4.5],
"robotType":9
}
```

### 三轴直角机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * X轴转换比 / 360；第二位公式：1 * Y轴转换比 / 360；第三位公式：1 * Z轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / X轴转换比 * 360；第二位公式：1 / Y轴转换比 * 360；第三位公式：1 / Z轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"conversionRatio_X":100.0,
"conversionRatio_Y":90.0,
"conversionRatio_Z":80.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[0.277777777778,0.25,0.222222222222],
"distanceToAngle":[3.6,4.0,4.5],
"robotType":10
}
```

### 三轴直角异型1

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "conversionRatio2" | double | 二轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio3" | double | 三轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第二位公式：1 * 二轴转换比 / 360；第三位公式：1 * 三轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第二位公式：1 / 二轴转换比 * 360；第三位公式：1 / 三轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"conversionRatio2":100.0,
"conversionRatio3":100.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,0.277777777778,0.25],
"distanceToAngle":[1.0,3.6,4.0],
"robotType":11
}
```

### 二轴SCARA

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L2":120.0,
"L3":120.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0],
"distanceToAngle":[1.0,1.0],
"robotType":8
}
```

### 七轴串联多关节

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "Link" | string | DH参数列表 |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"Link":
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0
},
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0,1.0],
"robotType":12
}
```

### 龙门焊接模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * X轴转换比 / 360；第二位公式：1 * Y轴转换比 / 360；第三位公式：1 * Z轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / X轴转换比 * 360；第二位公式：1 / Y轴转换比 * 360；第三位公式：1 / Z轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L4":120.0,
"L5":120.0,
"conversionRatio_X":100.0,
"conversionRatio_Y":90.0,
"conversionRatio_Z":80.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0],
"distanceToAngle":[3.6,4.0,4.5,1.0,1.0],
"robotType":19
}
```

### 四轴并联机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000]；L2的值需要小于L3的值 |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":110.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0],
"robotType":20
}
```

### 酒槽机型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "L9" | double | L9杆长；double类型，范围[-4000,4000] |
| "L10" | double | L10杆长；double类型，范围[-4000,4000] |
| "L11" | double | L11杆长；double类型，范围[-4000,4000] |
| "L12" | double | 滑动电动缸导程；double类型，范围[-4000,4000] |
| "L13" | double | 顶升电动缸导程；double类型，范围[-4000,4000] |
| "L14" | double | 喷料距离；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * 滑动电动缸导程 / 360；第二位公式：1 * 顶升电动缸导程 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / 滑动电动缸导程 * 360；第二位公式：1 / 顶升电动缸导程 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"L8":120.0,
"L9":120.0,
"L10":120.0,
"L11":120.0,
"L12":100.0,
"L13":90.0,
"L14":120.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[0.277777777778,0.25,1.0,1.0],
"distanceToAngle":[3.6,4.0,1.0,1.0],
"robotType":21
}
```

### 龙门焊接2模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * X轴转换比 / 360；第二位公式：1 * Y轴转换比 / 360；第三位公式：1 * Z轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / X轴转换比 * 360；第二位公式：1 / Y轴转换比 * 360；第三位公式：1 / Z轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L4":120.0,
"L5":120.0,
"conversionRatio_X":100.0,
"conversionRatio_Y":90.0,
"conversionRatio_Z":80.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0],
"distanceToAngle":[3.6,4.0,4.5,1.0,1.0],
"robotType":22
}
```

### 四轴直角异型一

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "Link" | string | DH参数列表 |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "conversionRatio" | array | 轴转换比；double类型，范围[1,1000]；长度为2，第一个值为一轴转换比，第二个轴为四轴转换比 |
| "upsideDown" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * 一轴转换比 / 360；第四位公式：1 * 四轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / 一轴转换比 * 360；第四位公式：1 / 四轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"Link":
{
"L1":120.0,
"L2":120.0,
"conversionRatio":[100.0,90.0]
},
"upsideDown":false,
"robot":1,
"angleToDistance":[0.277777777778,1.0,1.0,0.25],
"distanceToAngle":[3.6,1.0,1.0,4.0],
"robotType":23
}
```

### 六轴龙门焊接模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "fiveAxisDirection" | double | 五轴方向；double类型，范围-90,0 度；0为五轴竖直向下，-90为五轴水平向右 |
| "upsideDown" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * X轴转换比 / 360；第二位公式：1 * Y轴转换比 / 360；第三位公式：1 * Z轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / X轴转换比 * 360；第二位公式：1 / Y轴转换比 * 360；第三位公式：1 / Z轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"conversionRatio_X":100.0,
"conversionRatio_Y":90.0,
"conversionRatio_Z":80.0,
"couplingRatio45":0.0,
"couplingRatio56":0.0,
"fiveAxisDirection":0.0,
"upsideDown":false,
"robot":1,
"angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0,1.0],
"distanceToAngle":[3.6,4.0,4.5,1.0,1.0,1.0],
"robotType":24
}
```

### 五轴混动机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "L9" | double | L9杆长；double类型，范围[-4000,4000] |
| "L10" | double | L10杆长；double类型，范围[-4000,4000] |
| "conversionratio_J1" | double | 1轴转换比；double类型，范围[-4000,4000] |
| "conversionratio_J2" | double | 2轴转换比；double类型，范围[-4000,4000] |
| "conversionratio_J3" | double | 3轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * 一轴转换比 / 360；第二位公式：1 * 二轴转换比 / 360；第三位公式：1 * 三轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / 一轴转换比 * 360；第二位公式：1 / 二轴转换比 * 360；第三位公式：1 / 三轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"L8":120.0,
"L9":0.0,
"L10":120.0,
"conversionratio_J1":100.0,
"conversionratio_J2":90.0,
"conversionratio_J3":80.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0],
"distanceToAngle":[3.6,4.0,4.5,1.0,1.0],
"robotType":25
}
```

### 四轴SCARA异型2

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | 1轴螺距；double类型，范围[-1000,0),(0,1000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "couplingRatio34" | double | 3/4耦合比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 3轴螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * 一轴螺距 / 360；第三位公式：1 * 三轴螺距 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / 一轴螺距 * 360；第三位公式：1 / 三轴螺距* 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":100.0,
"L2":120.0,
"L3":120.0,
"couplingRatio34":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1,
"angleToDistance":[0.277777777778,1.0,0.222222222222,1.0],
"distanceToAngle":[3.6,1.0,4.5,1.0],
"robotType":26
}
```

### 六轴异型三

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "L9" | double | L9杆长；double类型，范围[-4000,4000] |
| "L10" | double | L10杆长；double类型，范围[-4000,4000] |
| "L11" | double | L11杆长；double类型，范围[-4000,4000] |
| "L12" | double | L12杆长；double类型，范围[-4000,4000] |
| "L13" | double | L13杆长；double类型，范围[-4000,4000] |
| "L14" | double | L14杆长；double类型，范围[-4000,4000] |
| "L15" | double | L15杆长；double类型，范围[-4000,4000] |
| "L16" | double | L16杆长；double类型，范围[-4000,4000] |
| "L17" | double | L17杆长；double类型，范围[-4000,4000] |
| "L18" | double | L18杆长；double类型，范围[-4000,4000] |
| "L19" | double | L19杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":120.0,
"L7":120.0,
"L8":120.0,
"L9":120.0,
"L10":120.0,
"L11":120.0,
"L12":120.0,
"L13":120.0,
"L14":120.0,
"L15":120.0,
"L16":120.0,
"L17":120.0,
"L18":120.0,
"L19":120.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
"robotType":27
}
```

### 三轴SCARA异型一

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0],
"robotType":28
}
```

### delta2D并联机器人模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000]；L2的值需要小于L3的值 |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":110.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0],
"robotType":29
}
```

### 龙门焊接3模型

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "conversionRatio_X" | double | X轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Y" | double | Y轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio_Z" | double | Z轴转换比；double类型，范围[-4000,4000] |
| "threeAxisDirection" | double | 四轴方向；double类型，范围0,90 度；四轴方向为0时，L4应填0 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * X轴转换比 / 360；第二位公式：1 * Y轴转换比 / 360；第三位公式：1 * Z轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / X轴转换比 * 360；第二位公式：1 / Y轴转换比 * 360；第三位公式：1 / Z轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L4":120.0,
"L5":120.0,
"conversionRatio_X":100.0,
"conversionRatio_Y":90.0,
"conversionRatio_Z":80.0,
"mountAngle":false,
"robot":1,
"threeAxisDirection":90.0,
"angleToDistance":[0.277777777778,0.25,0.222222222222,1.0,1.0],
"distanceToAngle":[3.6,4.0,4.5,1.0,1.0],
"robotType":30
}
```

### 三轴串联异型一

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "threeAxisDirection" | double | 三轴方向；double类型，范围0,90 度 |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"mountAngle":false,
"robot":1,
"threeAxisDirection":90.0,
"angleToDistance":[1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0],
"robotType":31
}
```

### 五轴协作机器人

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000]；L2请填负值 |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000]；L6请填负值 |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":-120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":-120.0,
"L7":120.0,
"L8":120.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0,1.0],
"robotType":32
}
```

### 四轴SCARA异型3

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "couplingRatio12" | double | 1/2耦合比；double类型，范围[-1000,1000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "pitch" | double | 螺距；double类型，范围[-1000,0),(0,1000] |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * 螺距 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / 螺距 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"L3":120.0,
"L4":120.0,
"couplingRatio12":0.0,
"mountAngle":false,
"pitch":80.0,
"robot":1,
"angleToDistance":[0.222222222222,1.0,1.0,1.0],
"distanceToAngle":[4.5,1.0,1.0,1.0],
"robotType":33
}
```

### 六轴串联-CBBARA

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000]；L2请填负值 |
| "L3" | double | L3杆长；double类型，范围[-4000,4000] |
| "L4" | double | L4杆长；double类型，范围[-4000,4000] |
| "L5" | double | L5杆长；double类型，范围[-4000,4000] |
| "L6" | double | L6杆长；double类型，范围[-4000,4000] |
| "L7" | double | L7杆长；double类型，范围[-4000,4000] |
| "L8" | double | L8杆长；double类型，范围[-4000,4000] |
| "couplingRatio45" | double | 4/5耦合比；double类型，范围[-1000,1000] |
| "couplingRatio46" | double | 4/6耦合比；double类型，范围[-1000,1000] |
| "couplingRatio56" | double | 5/6耦合比；double类型，范围[-1000,1000] |
| "upsideDown" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":-120.0,
"L3":120.0,
"L4":120.0,
"L5":120.0,
"L6":0.0,
"L7":0.0,
"L8":120.0,
"couplingRatio45":0.0,
"couplingRatio46":0.0,
"couplingRatio56":0.0,
"upsideDown":false,
"robot":1,
"angleToDistance":[1.0,1.0,1.0,1.0,1.0,1.0],
"distanceToAngle":[1.0,1.0,1.0,1.0,1.0,1.0],
"robotType":34
}
```

### 高格立柱旋转四轴

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| "L1" | double | L1杆长；double类型，范围[-4000,4000] |
| "L2" | double | L2杆长；double类型，范围[-4000,4000] |
| "conversionRatio1" | double | 1轴转换比；double类型，范围[-4000,4000] |
| "conversionRatio2" | double | 3轴转换比；double类型，范围[-4000,4000] |
| "mountAngle" | bool | 机器人正装或倒装；bool类型；false表示正装，true表示倒装 |
| "robot" | double | 当前机器人号；int类型，范围[1,4] |
| "angleToDistance" | array | 机器人角度转距离列表；double类型；长度为当前机器人的轴数；第一位公式：1 * 一轴转换比 / 360；第三位公式：1 * 三轴转换比 / 360 |
| "distanceToAngle" | array | 机器人距离转角度列表；double类型；长度为当前机器人的轴数；第一位公式：1 / 一轴转换比 * 360；第三位公式：1 / 三轴转换比 * 360 |
| "robotType" | double | 当前机器人类型；int类型 |

```json
{
"L1":120.0,
"L2":120.0,
"conversionRatio1":100.0,
"conversionRatio2":100.0,
"mountAngle":false,
"robot":1,
"angleToDistance":[0.277777777778,1.0,0.25,1.0],
"distanceToAngle":[3.6,1.0,4.0,1.0],
"robotType":35
}
```

---

## 上位机请求保存预置机器人参数

**命令字：0x20C3**


---

## 控制器回复上位机保存预置机器人参数结果

**命令字：0x20C4**


---

## 上位机发送设置机器人关节参数

**命令字：0x20C5**


---

## 上位机查询机器人关节参数

**命令字：0x20C6**


---

## 控制器回复上位机机器人关节参数

**命令字：0x20C7**


---

## 上位机发送设置机器人笛卡尔参数

**命令字：0x20C8**


---

## 上位机查询机器人笛卡尔参数

**命令字：0x20C9**


---

## 控制器回复上位机机器人笛卡尔参数

**命令字：0x20CA**


---

## 上位机设置机器人关节多圈值参数

**命令字：0x20CB**


---

## 上位机查询机器人编码器多圈值参数

**命令字：0x20CC**


---

## 控制器回复上位机机器人编码器多圈值参数

**命令字：0x20CD**


---

## 上位机申请另存为预置机器人参数文件

**命令字：0x20CE**


---

## 上位机查询预置机器人文件列表

**命令字：0x20CF**


---

## 控制器回复上位机预置机器人文件列表

**命令字：0x20D0**


---

## 上位机发送获取预置参数请求

**命令字：0x20D1**


---

## 控制器回复机器人已保存的预置机器人参数

**命令字：0x20D2**


---

## 上位机发送酒槽机型标记圆心请求

**命令字：0x20D3**
