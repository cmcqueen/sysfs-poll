sysfs-poll
==========

This provides example code for using the poll() function on Linux to poll an attribute in the sysfs file system.

Only some sysfs attributes support polling using this method. One example would be the 'value' attribute of an exported GPIO configured as an input (although the sysfs interface for GPIO is now deprecated). Eg:

    cd /sys/class/gpio
    echo 123 > export
    cd gpio123
    echo "in" > direction
    sysfs-poll value
