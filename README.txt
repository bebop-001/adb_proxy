This is a simple PERL front end for adb which supports
USAGE of adb_proxy:
    install   : install package: Install and start the apk file passed in.
    list      : Print a list of found devices and exit.
    ls        : Execute the ls command on the target.
    packages  : packages <regex>  List packages found on the device.
                Filter using <regex> if one is given.
    pull      : device_file host_file
                Read device_file from the device to host_file.
    push      : host_file device_file    host_file device_file
                Copy the host_file to the device_file.
    reset     : <-s>   Reset ADB abd display detected devices.  If <-s> is set,
                reset is executed as root.  'Reset' means adb kill-server;
                adb start-server; adb devices.
    shell     : device_file host_file    Execute a shell command on host.
    uninstall : unistall package: remove the apk indicated by the package.

I use it on Linux.  It might run on CPAN under windows but I don't know.

