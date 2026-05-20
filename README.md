# ESP32 LILYGO-mlx90632 Release

---

## Android APK / LILYGO MLX BLE v1.0.0

| File | Description |
|---|---|
| `apk/LILYGO_MLX_v1.0.0_debug.apk` | Version-specific APK |
| `apk/LILYGO_MLX_latest.apk` | Latest APK (fixed URL) |

### APK 기능
- BLE 스캔 & 연결 (ESP32 LILYGO)
- MLX90632 실시간 온도 수신 (To / Ta)
- 실시간 라인 차트
- CSV 로그 저장 & 공유

### BLE 데이터 포맷 (ESP32 → Android)
```json
{"to": 36.5, "ta": 25.3}
```

---

## esp32 / MLX_TempDisplay v2.1.0

| File | Description |
|---|---|
| `esp32/MLX_TempDisplay_v2.1.0.bin` | Version-specific firmware |
| `esp32/MLX_TempDisplay_latest.bin` | Latest firmware (fixed URL) |

### Fixed Download URL
`https://github.com/seatoskymee/ESP32_LILYGO-mlx90632-Release/releases/latest/download/MLX_TempDisplay_latest.bin`

### Flash Command (esptool)
```
esptool.py --chip esp32 --port COM30 --baud 921600 write_flash -z 0x10000 MLX_TempDisplay_latest.bin
```

### Features (v2.1.0)
- MLX90632 contactless temperature sensor (To / Ta)
- BLE NUS with bonding & auto-reconnect (NimBLE)
- WiFi AP management with NVS preferred list
- Web dashboard (/) + WiFi management (/wifi)
- Firebase Realtime Database upload
- LCD ST7789V 240×135 live display
- Dual-button WiFi menu (scan / connect / preferred list / clear)
