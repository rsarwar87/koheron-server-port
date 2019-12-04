# PORTING KOHERON SERVER TO OTHER DEVICES

Sometimes it is too complicated to port a given board to a koheron SDK. for those cases, it is just easier to take the 
koheron-server stack to the device.  

Supports Zynq and ZynqMP

Contains the client side python and cpp drivers

## Procedure to compile server
1. Prepare a config.yml file to the which contains the list of control_registers, status_registers, parametes, drivers and memory tags. The memory tags must correspond to the Address Map on the actual device

2. Make autogenerated files needed.
``` 
make CONFIG=python server
```

3. Prepare the build directory and make the software
```
mkdir build
cd build
make ../ -DCMAKE_TOOLCHAIN_FILE=../toolchain-zynq.cmake 
make
```

## Procedure to compile cpp client

## Procedure to port control and status ip

