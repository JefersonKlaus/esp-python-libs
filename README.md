### Jeferson Klaus - jefersonklaus@gmail.com ###

# esp-python-libs


## Whas is this project:
This project was developed to simplify the python code when using peripherals in ESP32.


## Usage

```python
# JOYSTIC
from joystick import Joystick
joystick = Joystick(pin_x=36, pin_y=39, pin_z=14)
print(joystick.get_x_value())
print(joystick.get_y_value())
print(joystick.get_z_value())


# LED BARD
from led_bar import LedBar
led_bar = LedBar(pin_list=[15, 2, 0, 4, 5, 18, 19, 21, 22, 23])
led_bar.turn_on_in_scale(value=50, in_scale_min=0, in_scale_max=100)


# POTENTIOMETER
from potentiometer import Potentiometer
potentiometer = Potentiometer(pin=36)
print(potentiometer.get_value_in_scale(out_scale_min=0, out_scale_max=100)


# SERVO
from servo import Servo
servo = Servo(pin_number=15, max_degree=180, freq=50, nit_duty=0)
servo.set_degree(degree=180)


# SONAR
from sonar import Sonar
sonar = Sonar(pin_in=14, pin_out=13)
sonar.distance_mm()
sonar.distance_cm()


# LCD I2C
from lcs import I2cLcd
lcd = I2cLcd(scl_pin=14, sda_pin=13)
lcd.move_to(0, 0)
lcd.put_str("Temp.      %.2f" % temperatura)
lcd.move_to(0, 1)
lcd.put_str("Humidade   %.2f" % humidity)


# SEP MOTOR
from stepmotor import Stepmotor, StepMotorDirectionOptions
step_motor = Stepmotor(A=32, B=33, C=25, D=26)
step_motor.move_steps(StepMotorDirectionOptions.CLOCKWISE, 32 * 64)
step_motor.move_degree(StepMotorDirectionOptions.CLOCKWISE, 720)
step_motor.stop()


# THERMISTOR
from thermistor import Thermistor
from thermistor import Thermistor
thermistor = Thermistor(pin=36)
print(thermistor.get_temperature())
```