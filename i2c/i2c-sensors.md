# I2C sensors

## Supported sensors

### IMU sensors

If you do not have an electronic compass on board you will need an IMU. An Inertial Measurement Unit, or IMU, measures and reports on velocity, orientation and gravitational forces, using a combination of an accelerometer, gyroscope, and a magnetometer. Connecting an IMU to OpenPlotter will provide magnetic heading which is needed to calculate true heading and true wind. You will have heel and trim angle data as well.

![](../.gitbook/assets/imu.png)

* InvenSense MPU-9150 single chip IMU
* InvenSense MPU-6050 plus HMC5883 magnetometer on MPU-6050's aux bus \(handled by the MPU-9150 driver\)
* InvenSense MPU-6050 gyros + acclerometers. Treated as MPU-9150 without magnetometers
* **InvenSense MPU-9255 single chip IMU**
* **InvenSense MPU-9250 single chip IMU**
* STM LSM9DS0 single chip IMU
* STM LSM9DS1 single chip IMU
* L3GD20H + LSM303D \(optionally with the LPS25H\) as used on the Pololu AltIMU-10 v4
* L3GD20 + LSM303DLHC as used on the Adafruit 9-dof \(older version with GD20 gyro\) IMU
* L3GD20H + LSM303DLHC \(optionally with BMP180\) as used on the new Adafruit 10-dof IMU
* Bosch BMX055 \(although magnetometer support is experimental currently\)
* Bosch BNO055 IMU with onchip fusion. Note: will not work reliably with RaspberryPi/Pi2 due to clock-stretching issues

{% hint style="success" %}
We recommend MPU-9255 and MPU-9250. OpenPlotter code is optimized for these IMUs
{% endhint %}

{% hint style="info" %}
You have to configure IMU sensors in [pypilot](https://docs.sailoog.com/openplotter-v1-x-x/pypilot) tab. The rest of I2C sensors are configured in [I2C](https://docs.sailoog.com/openplotter-v1-x-x/i2c) tab
{% endhint %}

### Environment sensors

![](../.gitbook/assets/bme280.jpg)

* BMP180: pressure, temperature 
* **BME280: pressure, temperature, humidity** 
* LPS25H: pressure, temperature 
* MS5611: pressure, temperature 
* MS5637: pressure, temperature 
* HTS221: humidity, temperature 
* HTU21D: humidity, temperature 
* MS5607-02BA03: pressure, temperature

{% hint style="success" %}
We recommend BME280
{% endhint %}

## Connecting I2C sensors

I2C sensors are connected in parallel to the **SDA**, **SDL**, **GND** and **3.3V** GPIO of your Raspberry.

![](../.gitbook/assets/i2c_sensors.png)

![](../.gitbook/assets/rp2_pinout.png)

