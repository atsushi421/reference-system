# Edit maximum number for pseudo-work
Edit value in lines 42~ in `./autoware_reference_system/include/autoware_reference_system/system/timing/default.hpp`

# Set number of cores
```
$ cat /proc/cpuinfo | grep processor
$ sudo bash ~/reference-system/enable_cpucores.sh [NUMBER_OF_CORES]
$ cat /proc/cpuinfo | grep processor
```

# Run and trace autoware reference system
```
$ sudo sysctl -w net.core.rmem_max=2147483647 && sudo ifconfig lo multicast && source ~/reference-system/install/local_setup.bash && source ~/reference-system/install/setup.bash && cd reference-system && ros2 launch autoware_reference_system reference_system_single.launch.py
```
