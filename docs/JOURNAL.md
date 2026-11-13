# Project journal — AUTO-BALANCING YAHBOOM

## 2026-11-13 — Repository creation

- Public GitHub repository created from an empty folder. `README.md`, `.gitignore` and this journal are on
  GitHub; `CLAUDE.md`, `firmware/` and `hardware/` stay local for now
  (owner's choice).
- Repository language: English for docs, commit messages and code comments.
- No code or measurements yet.

### Base hardware

The robot is built from a dismantled **Yahboom ROSMASTER X3** (mecanum wheels): Jetson Nano 4 GB
(B01), Yahboom expansion board (motors + power + IMU), encoder gear motors, Orbbec Astra camera.
The X3 itself is not the goal: it is the parts donor for the self-balancing robot.

### Open questions

- Which IMU is on the expansion board, and can the board run the balance loop itself, or must the
  loop run on the Jetson (latency over the serial link)?
- Mecanum wheels are poor for balancing (rollers): keep them for a first test or swap for plain
  wheels?
- Frame: where to mount the Jetson and battery (higher centre of mass is easier to balance but
  needs more torque).

### To do

1. Dismantle the X3, identify the expansion board and IMU, record the wiring in `hardware/`.
2. Add the firmware to `firmware/` and document building / flashing.
3. Tune the balance PID (log every gain set tried and its result here).
4. Add the speed and steering loops, then remote control.
