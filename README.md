# Package Handling System / Delivery Truck project with Gradle

## About this project

This repository stores a template project about `Delivery Truck`. You will use this project to get started and will add your developed software to this project. 

## Getting Started

Once you download in your computer the project, open Java IDE [IntelliJ](https://www.jetbrains.com/idea/))
to import this [Gradle](https://gradle.org/) project. The project includes latest dependencies and
an example ready to be deployed on Delivery Truck using the `Delivery Truck` library from `CONNEX-AB-Delivery-System`.
The project includes some tasks to reduce the time to deploy on your robot.

Review the IP of your Brick and update the file `deploy.gradle`:

```
remotes {
    ev3dev {
        host = '192.168.1.180'
        user = 'robot'
        password = 'maker'
    }
}
```

The tasks associated to deploy on your robot are:

- deploy (The project deliver a FatJar to your Brick)
- remoteRun (Execute a jar deployed on your Brick)
- deployAndRun (Deploy & Execute from your Computer the program that you configured on the file: MANIFEST.MF)

You can use the Java IDE to launch the task or execute them from the terminal

```
./gradlew deployAndRun
```

# General help info

## Getting Started

LEGO brick is running on Debian-based operating system ev3dev: https://github.com/ev3dev (for more info see ev3dev links).

And is programmed in JAVA: http://ev3dev-lang-java.github.io/#/. JAVA programms are deployed on brick by using Gradle,
to see how it is done, follow this link: http://ev3dev-lang-java.github.io/docs/support/getting_started/create-your-first-project.html.
(also Git repo for example source code available here: https://github.com/ev3dev-lang-java/template_project_gradle).

## Modify the example

In order to modify the example, current full APIs are:

http://ev3dev-lang-java.github.io/docs/api/latest/index.html

You mostly will use EV3 Sensors in package: ev3dev.sensors.ev3 <br />
And classes: EV3ColorSensor, EV3IRSensor, EV3TouchSensor, EV3UltrasonicSensor <br />
*note: we also will use custom LineReaderV2 class, documentation here: TODO: LINK <br />


You mostly will use EV3 Motors in package: ev3dev.actuators.lego.motors <br />
And classes: EV3LargeRegulatedMotor, EV3MediumRegulatedMotor



## Examples

Exist several examples ready to use here:

https://github.com/ev3dev-lang-java/examples

## Sensors and Motors

For ev3dev OS capabilities on EV3Brick and BrickPI3, you can read here: http://docs.ev3dev.org/en/ev3dev-jessie/

You can learn about sensor capabilities here: http://docs.ev3dev.org/projects/lego-linux-drivers/en/ev3dev-jessie/sensor_data.html

You can learn about sensor capabilities here: http://docs.ev3dev.org/projects/lego-linux-drivers/en/ev3dev-jessie/motor_data.html

Hint: value0 -> value(0) in Java.

## Network

If necessary, to set-up wifi, you can access robot through ssh and then use "connman", described here (Section: Connecting to an open access point):  https://wiki.archlinux.org/index.php/ConnMan#Connecting_to_an_open_access_point
