# Bee@C3LAB cfclient baseline

Source: https://github.com/qljz1993/crazyflie-clients-python

Baseline commit: `76d509343d37bd6e0292adb62295d8deb0fc7d1a`

Bee changes retain the existing Python packaging compatibility fixes and use
importlib.metadata to read the installed client version on modern Python.
Setuptools remains below version 81 because the paired cflib imports
pkg_resources.

The flight tab labels explicit arming as unsupported for older firmware
protocol versions, including ESP-Drone. The parent Bee@C3LAB repository
provides the Docker environment and pins the matching modified cflib revision.
