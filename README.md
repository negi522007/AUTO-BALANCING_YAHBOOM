# AUTO-BALANCING YAHBOOM — Self-balancing robot (TEKBOT)

TEKBOT project: turn the parts of a **Yahboom ROSMASTER X3** (mecanum-wheel ROS robot) into a
**self-balancing robot** (two-wheeled inverted pendulum). The X3 is dismantled and its parts are
reused. The robot stays upright on its own by measuring its tilt with an inertial measurement unit and
continuously correcting its motor speed (PID control, inverted pendulum principle).

## 🔩 Hardware (from the ROSMASTER X3)

| Part | Details |
|---|---|
| Compute board | NVIDIA Jetson Nano 4 GB (B01) |
| Motor / power board | Yahboom expansion board (onboard IMU, model to confirm) |
| Motors | X3 encoder gear motors (2 of the 4 reused for balancing) |
| Wheels | Mecanum wheels from the X3, to be replaced by plain wheels if they hurt balancing |
| Camera | Orbbec Astra (RGB + depth), optional |

## 🎯 Goals

1. Keep the robot upright and stable (balance loop).
2. Add the speed loop and the steering loop (move forward, backward and turn without falling).
3. Drive the robot remotely (Bluetooth / app).
4. Document the PID tuning so that others can reproduce it.

## 🧠 How it works

```
IMU (expansion board) →  tilt angle (complementary / Kalman filter)
                      →  balance PID  ─┐
Wheel encoders        →  speed PID    ─┼→  PWM command  →  motor driver  →  motors
Gyroscope (Z axis)    →  steering PID ─┘
```

## 🚧 Status

Repository initialised. Next: dismantle the X3, choose the two-wheel layout, then write the balance
loop. See [`docs/JOURNAL.md`](docs/JOURNAL.md).
