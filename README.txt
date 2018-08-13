This is a simple PERL front end for adb which supports
USAGE of adb_proxy:
    To run a function on one or more devices, run
        "adb_proxy device_0 ... device_n command ..."
    To run a function on all devices, run
        "adb_proxy all command..."
    Possible commands are:
    install   : install package: Install t the apk files passed in.
        If the first arg is '-s', start the apk.  NOTE! if more
        than one apk file is passed in, only the last is started.

    ls        : Execute the ls command on the target.

    packages  : packages <regex>  List packages found on the device.
        Filter using <regex> if one is given.

    permissions : permissions <regex> [revoke|grant a]
        If neither grant or revoke are given, list granted
        permissions. If grant or revoke is requested and 'a'
        is requested, grant/revoke all privelages.  If 'a' is not
        set, allow user to select privalage to grant/revoke.
        The regex allows the user to select the package to operate
        on.

    pull      : device_file host_file
        Read device_file from the device to host_file.

    push      : host_file device_file
        host_file device_file    Copy the host_file to the device_file.

    reset     : <-s>   Reset ADB abd display detected devices.  If <-s> is set,
        reset is executed as root.  'Reset' means adb kill-server;
        adb start-server; adb devices.
    restart   : regex_for_package
        Stop and then restart the app based on the package selected
        by the regex.

    shell     : device_file host_file
        Execute a shell command on host.

    start     : Start the app associated with the apk file passed in.
        If the first arg is '-s', start the apk.

    stop      : regex_for_package
        Stop and the app based on the package selected
        by the regex.

    uninstall : unistall package: remove the apk indicated
        by the package regex passed in.

I use it on Linux.  It might run on CPAN under windows but I don't know.

