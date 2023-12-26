# mp135

|   | 厂家 | 型号 | 目录 |
|---|---|---|---|
| 芯片(soc) | st | stm32mp135 | device/soc/st/stm32mp135 |
| 开发板(board) | atk | atk-dlmp135 | device/board/atk/atk-dlmp135 |
| 产品(product) | yhuan | mp135_standard | vendor/yhuan/mp135_standard |

# 创建相关目录
``` sh
mkdir -p device/soc/st/stm32mp135
mkdir -p device/board/atk/atk-dlmp135
mkdir -p vendor/yhuan/mp135_standard
```

# 创建config.json
``` json
{
    "product_name": "mp135_standard",
    "device_company": "atk",
    "device_build_path": "device/board/atk/atk-dlmp135",
    "target_cpu": "arm",
    "type": "standard",
    "version": "3.0",
    "board": "atk-dlmp135",
    "api_version": 8,
    "enable_ramdisk": true,
    "build_selinux": true,
    "build_seccomp": true,
    "inherit": [
        "productdefine/common/inherit/rich.json"
    ],
    "subsystems": [
        {
            "subsystem": "security",
            "components": [
                {
                    "component": "selinux",
                    "features": []
                }
            ]
        }
    ]
}
```