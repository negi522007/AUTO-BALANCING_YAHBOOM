# AUTO-BALANCING YAHBOOM — Self-balancing robot (TEKBOT)

TEKBOT project built around the **Yahboom self-balancing robot** (two-wheeled inverted pendulum):
the robot stays upright on its own by measuring its tilt with an inertial measurement unit and
continuously correcting its motor speed (PID control, inverted pendulum principle).

## 🎯 Goals

1. Keep the robot upright and stable (balance loop).
2. Add the speed loop and the steering loop (move forward, backward and turn without falling).
3. Drive the robot remotely (Bluetooth / app).
4. Document the PID tuning so that others can reproduce it.

## 🧠 How it works

```
IMU sensor (MPU6050)  →  tilt angle (complementary / Kalman filter)
                      →  balance PID  ─┐
Wheel encoders        →  speed PID    ─┼→  PWM command  →  motor driver  →  motors
Gyroscope (Z axis)    →  steering PID ─┘
```

## 🚧 Status

Repository initialised: the exact Yahboom board, the firmware and the tuning values are still to come.
