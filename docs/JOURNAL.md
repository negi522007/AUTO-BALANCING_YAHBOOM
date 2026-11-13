# Project journal — AUTO-BALANCING YAHBOOM

## 2026-11-13 — Repository creation

- Public GitHub repository created from an empty folder. `README.md`, `.gitignore` and this journal are on
  GitHub; `CLAUDE.md`, `firmware/` and `hardware/` stay local for now
  (owner's choice).
- Repository language: English for docs, commit messages and code comments.
- No code or measurements yet.

### Open questions

- Exact Yahboom kit model (Arduino UNO/Nano or STM32 board, TB6612 or other driver, MPU6050 IMU,
  encoder motors)? Needed to pick the toolchain (Arduino IDE, PlatformIO or Keil/STM32CubeIDE).
- Start from Yahboom's sample code or rewrite the control loop?

### To do

1. Identify the board and record the pinout in `hardware/`.
2. Add the firmware to `firmware/` and document building / flashing.
3. Tune the balance PID (log every gain set tried and its result here).
4. Add the speed and steering loops, then remote control.
