# nvp  

https://player.vimeo.com/video/570963981?title=0&amp;byline=0&amp;portrait=0 

https://github.com/google/android-cuttlefish/blob/main/BUILDING.md#adb
## ADB

When the adb client is running outside the container either remotely or locally (on the docker host), the cuttlefish inside the container
could be accessed as follows:

```bash
adb connect $ip_cf1:6520
adb shell
```

Please note that --norun_adb_connector should have been given to the cvd_start_<name> command. Also, ```$ip_cf1``` is the public or internal
ip address of the container. 

Alternatively, you could run adb inside the container, and use the adb client over ssh:

```bash
ssh vsoc-01@$ip_cf1 -- ./bin/adb -e shell
