# ESP32 LILYGO-mlx90632 Release

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
