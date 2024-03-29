# Guide/Tweaks for ANDROID phones without root.

### Intro
* Hello Good Day everyone.
I am pleased to announced that you can tweak some Android
settings without root permissions Yay. Someone can try other
phones but this works on my xiaomi mi A3 and A1. BOTH of my
phones are not rooted neither are they unlocked. I borrowed my
friends J7 prime and got some working there too. Your mileage may
vary. It should work the same on most phones. I tried some stuff
and this is my findings. Some tweaks require that you Write
secure settings through adb. I am not taking responsibility if
you try and you damage your phone. Do this at your own risk.
Thank you.

If you delete the app or uninstall you lose all your settings.

If you do want to undo changes just delete setting line.

For best user experience use all working tweaks. Or you can
choose what you want or do not want it is up to you. Your mileage
still may vary.

OTA UPDATES don't affect settings on my phone neither do they
conflict with manufacturers settings. There are some new settings
line enabled on android properties that made some of my added
tweaks on system tables redundant so I just deleted those
redundant ones from system table. Will do some further
investigating YOU can always COMPARE android properties with the
tweaks you are adding to see if you are adding redundant comands.
Android is forever improving, rooting is becoming obsolete, for
the not pickers, a lot of these tweaks may not be necessary in
the future because android might have them as standard but until
then this is necessary to get the best out of your phone or to
get the things you want and not what Google gives you. Thank you

### LETS BEGIN

* Open Settings Database Editor, select system table.

* Add new settings
    ro.config.hw_quickpoweron  true
    boot.fps 25
    debug.sf.nobootanimation 1

* Reboot phone.
* Enjoy faster boot.

### More working tweaks

* Display density
(Trust me on this for mi a3 IDK why but it does. For other phones
add whatever you are comfortable with or is recommended.)
    display_density_forced 209

* Ring without delay
    ring.delay 0

* Faster boot under 10 seconds.
(Range from 15 to 30 depending on how fast your processor is.)
    boot.fps 25
    debug.sf.nobootanimation 1

* Wifi scan interval
(Increases time between WiFi scans, saves battery and CPU power.)
    wifi.supplicant_scan_interval 120

* Power savings
    pm.sleep_mode 1
    power_supply.wakeup enable

* Gaming/3d performance.
    debug.enabletr true
    debug.qctwa.preservebuf 1
    dev.pm.dyn_samplingrate 1
    video.accelerate.hw 1
    debug.overlayui.enable 1
    debug.egl.hw 1
    Debug.egl.prifiler 1
    debug.sf.hw 1
    debug.composition.type c2d
    debug.composition.type gpu
    debug.performance.tuning 1

* Better navigation scrolling speed
    windowsmgr.max_events_per_sec 100

* Disable fingerprint reader animation.
    fod_animation_type 4

* disable logcat
    Logcat.live disable

* Enhance Sound quality
    af.resampler.quality 255
    mpq.audio.decode true

* Internet browsing and download.
    net.tcp.buffersize.default 4096,87380,256960,4096, 16384,256960
    net.tcp.buffersize.wifi 4096,87380,256960,4096,163 84,256960
    net.tcp.buffersize.umts 4096,87380,256960,4096,163 84,256960
    net.tcp.buffersize.gprs 4096,87380,256960,4096,163 84,256960
    net.tcp.buffersize.edge 4096,87380,256960,4096,163 84,256960
    net.tcp.buffersize.hspa 6144,87380,524288,6144,163 84,262144
    net.tcp.buffersize.lte 524288,1048576,2097152,5242 88,1048576,2097152
    net.tcp.buffersize.hsdpa 6144,87380,1048576,6144,8 7380,1048576
    net.tcp.buffersize.evdo_b 6144,87380,1048576,6144, 87380,1048576
    net.rmnet0.dns1 8.8.8.8
    net.rmnet0.dns2 8.8.4.4
    net.dns1 8.8.8.8
    net.dns2 8.8.4.4
    net.ppp0.dns1 8.8.8.8
    net.ppp0.dns2 8.8.4.4
    net.wlan0.dns1 8.8.8.8
    net.wlan0.dns2 8.8.4.4
    net.eth0.dns1 8.8.8.8
    net.eth0.dns2 8.8.4.4
    net.gprs.dns1 8.8.8.8
    net.gprs.dns2 8.8.4.4

* Note
(You can use whAtever dns is faster for u for example cloud share dns1)
    1.1.1.1 dns2 1.0.0.1

* Enable GPU Acceleration
(avoid enabling this in developer mode it resets when phone
restarts)
    debug.qc.hardware true
    debug.qctwa.statusbar 1
    debug.qctwa.preservebuf 1
    debug.composition.type gpu
    hw3d.force 1
    hwui.render_dirty_regions false
    hwui.disable_vsync true

* Haptic feedback
(0 is off and 1 is on. 0 disables boot vibration as well.)
    haptic_feedback_enabled 0


* Touch sensitivity
    touch.presure.scale 0.001
    debug.egl.profiler 1

* Dalvik Virtual Machine tweaks.
(Better performance of device overall)
    dalvik.vm.checkjni false
    dalvik.vm.dexopt-data-only 1
    dalvik.vm.heapstartsize 5m
    dalvik.vm.heapgrowthlimit 48m
    dalvik.vm.heapsize 64m
    dalvik.vm.verify-bytecode false
    dalvik.vm.execution-mode int:jit
    dalvik.vm.lockprof.threshold 250
    dalvik.vm.dexopt-flags m=v,o=y
    dalvik.vm.stack-trace-file /data/anr/traces.txt
    dalvik.vm.jmiopts forcecopy

* Smoother video streaming and tweak media
    media.stagefright.enable-player true
    media.stagefright.enable-meta true
    media.stagefright.enable-scan true
    media.stagefright.enable-http true
    media.stagefright.enable-aac true
    media.stagefright.enable-qcp true
    media.stagefright.enable-record true

* Wireless Tweaks
    net.ipv4.ip_no_pmtu_disc=0
    net.ipv4.route.flush=1
    net.ipv4.tcp_ecn=0
    net.ipv4.tcp_fack=1
    net.ipv4.tcp_mem=187000 187000 187000
    net.ipv4.tcp_moderate_rcvbuf=1
    net.ipv4.tcp_no_metrics_save=1
    net.ipv4.tcp_rfc1337=1
    net.ipv4.tcp_rmem=4096 39000 187000
    net.ipv4.tcp_sack=1
    net.ipv4.tcp_timestamps=1
    net.ipv4.tcp_window_scaling=1
    net.ipv4.tcp_wmem=4096 39000 18700

* This removes fps cap (TRY AT YOUR OWN RISK) I run this doh it's
  fine.
    debug.gr.swapinterval 0

### 22 Useful Android Build Prop Tweaks For Better Experience

22. Better Scrolling
You might have noticed your phone is not that smooth while
scrolling the screen. You can fix this by altering the minimum
and maximum fluid velocity. This will improve your overall
scrolling experience.

    windowsmgr.max_events_per_sec=150
    ro.min_pointer_dur=8
    ro.max.fling_velocity=12000
    ro.min.fling_velocity=8000
    persist.sys.scrollingcache=3
    debug.sf.hw=1

21. Auto Rotation for Homescreen and Lockscreen
The new versions of Android do not support auto-rotation on
lockscreen. Likewise, Numerous OEM launchers and stock launchers
do not have auto-rotation support for the homescreen. Well, there
is absolutely nothing to worry about. You can enable these
rotations functionality by adding this command –

    lockscreen.rot_override=true  // for Lockscreen
    log.tag.launcher_force_rotate=VERBOSE  // for Homescreen

20. Better Internet Speed
If your browsing speed is not up to the mark on any Android
device you are using, or if you are suffering from slow download
speed, you can improve it by increasing the TCP’s buffersize.
Also, forcing the device to use Google’s DNS could unlock more
speed.

    net.tcp.buffersize.default=4096,87380,256960,4096, 16384,256960
    net.tcp.buffersize.wifi=4096,87380,256960,4096,163 84,256960
    net.tcp.buffersize.umts=4096,87380,256960,4096,163 84,256960
    net.tcp.buffersize.gprs=4096,87380,256960,4096,163 84,256960
    net.tcp.buffersize.edge=4096,87380,256960,4096,163 84,256960
    net.rmnet0.dns1=8.8.8.8
    net.rmnet0.dns2=8.8.4.4
    net.dns1=8.8.8.8
    net.dns2=8.8.4.4

19. Modify Logcat
You can control the Android Logcat file generation, which is
mainly used for debugging. Disabling logcat would reduce
expensive disk reads/writes.

    logcat.live=disable

18. Disable Black Screen Issue After Call
You might have noticed a black screen for a few seconds after you
disconnect a voice call. If this is happening to you on a regular
basis, it means your device’s proximity sensor is not functioning
properly. It can be fixed by changing the proximity delay value.

    mot.proximity.delay=0
    ro.lge.proximity.delay=25

17. Ring Your Phone Immediately
When you get a call, the Android system usually waits and
verifies the connection before it sends the signals to ring the
phone. However, if your device is taking more than a usual time
before it starts to ring, you can change this by adding the line
shown below.

    ro.telephony.call_ring.delay=0
    ring.delay=0

16. Improve Voice Call Clarity
You can control the AMR audio codec’s property, which is used for
voice calls. Also, you can adjust the volume of your voice calls.
By default, Android provides seven audio levels for calls. You
can change this number to manage it more precisely. The integer
value ranging between 7 and 20 is recommended.

    ro.ril.enable.amr.wideband=1
    ro.config.vc_call_steps=20

15. Improve Image Quality
In order to reduce the processing power, Android does not display
the entire content of an image. It only renders the picture at a
lower quality, which is good enough but not the best. If you
think your device has enough power to handle the image processing
task, you can force your hardware to display the original
quality.

    ro.media.enc.jpeg.quality=100

14. Increase Panorama Image Resolution
You can force the panorama mode in the camera app to save the
picture at a higher resolution. This may not be supported by all
devices.

    ro.media.panorama.defres=10800x2442
    ro.media.panorama.frameres=3264x1840

13. Quick Power On
When your device boots up, there are a lot of services that boot
up along with Android. The more applications you have, the longer
it would take. However, you can force your device to boot faster
by enabling “quickpoweron”, a process in which most of the data
is stored as a hibernation file, which is loaded upon the next
boot, saving a few seconds.

    ro.config.hw_quickpoweron=true

You can also disable the boot animation by adding the code below

    debug.sf.nobootanimation=1

12. Rotate Screen to 270 Degree
Most of the apps choose to rotate only 90°. However, the Android
system supports three default rotation degrees – 90°, 180°, and
270°. You can take leverage of this feature and force all your
apps to rotate 270°.

    windowsmgr.support_rotation_270=true

11. Modify Error Profiler
For most users, there is literally no use in having error
profiling. However, a few apps might make use of this for
generating error reports. You can enable or disable the error
profiler by adding the code shown below. Put 0 for enabling or 1
for disabling the feature.

    profiler.force_disable_err_rpt=1
    profiler.force_disable_ulog=1

10. Keep Key Lights On While Screen Is On
If your phone has backlit capacitive keys on it, you might have
noticed that the key lights usually turn off after a few seconds
you press it. If you want these key lights to be permanently
turned on as long as the screen stays awake, just change the
backlit’s timeout value.

    ro.mot.buttonlight.timeout=0

9. Keep Your Launcher In Memory
If you are using an Android Launcher app, you can force it to
stay in the main memory (RAM), by adding the following code. Your
device must have enough free memory for this, otherwise, you will
see lags and performance will be degraded severely.

    ro.HOME_APP_ADJ = 1

8. Save Power
Many Android devices come with built-in battery saving features
like Sony has “Stamina” and “Ultra Stamina” mode that cut
additional background services in order to save battery. You can
do it by yourself by adding this code.

    ro.mot.eri.losalert.delay=1000  //this may brake tethering
    ro.ril.power_collapse=1
    pm.sleep_mode=1
    wifi.supplicant_scan_interval=180
    ro.mot.eri.losalert.delay=1000
    power_supply.wakeup=enable
    ro.config.hw_fast_dormancy=1
    ro.config.hw_power_saving=1

7. Disable Automatic Error Reporting
App crashing is common on all platforms. Obviously, it doesn’t
feel good, but the continuous notification of error reporting is
even more frustrating. You can get rid of this built-in error
reporting function by adding the code shown below.

    profiler.force_disable_err_rpt=1
    profiler.force_disable_ulog=1

To disable error checking, use this –

    ro.kernel.checkjni=0
    ro.kernel.android.checkjni=0

And to disable the strict mode checking, add this line –

    persist.android.strictmode=0

6. Change Screen DPI
DPI stands for Dots Per Inch, which is also the ratio of your
device’s resolution to the display size. Usually, its values are
a multiple of 160, but you can set any value you want.

    ro.sf.lcd_density=420

5. Change WiFi Scan Interval
By default, Android scans for WiFi network at an interval of 15
seconds. In order to save battery, you can increase this interval
with the following code. The value is in seconds, so if you want
to change the interval to say 10 minutes, put 600, instead of
120.

    wifi.supplicant_scan_interval=120

4. Improve Gaming Experience
If you use your phone for extensive gaming, try adding the
following code at the end. This will enable tile rendering,
utilize processing power and improve 3d performance.

    persist.sys.NV_FPSLIMIT=60
    persist.sys.NV_POWERMODE=1
    persist.sys.NV_PROFVER=15
    persist.sys.NV_STEREOCTRL=0
    persist.sys.NV_STEREOSEPCHG=0
    persist.sys.NV_STEREOSEP=20
    persist.sys.purgeable_assets=1

    debug.enabletr=true
    debug.qctwa.preservebuf=1
    dev.pm.dyn_samplingrate=1
    video.accelerate.hw=1
    ro.vold.umsdirtyratio=20
    debug.overlayui.enable=1
    debug.egl.hw=1
    ro.fb.mode=1
    hw3d.force=1
    persist.sys.ui.hw=1
    ro.sf.compbypass.enable=0
    debug.sf.hw=1
    debug.composition.type=c2d
    persist.sys.composition.type=c2d
    debug.performance.tuning=1

    ro.media.dec.jpeg.memcap=8000000
    ro.media.enc.hprof.vid.bps=8000000
    ro.media.dec.aud.wma.enabled=1
    ro.media.dec.vid.wmv.enabled=1
    ro.media.cam.preview.fps=0
    ro.media.codec_priority_for_thumb=so

3. Modify MMS APN Retry Timer
If an SMS/MMS fails to send, Android tries to send it again after
5 seconds. You can change the number of reattempts and intervals
between those reattempts. The following code will force 3
retries, every 3 seconds.

    ro.gsm.2nd_data_retry_config=max/_retries=3, 3000, 3000, 3000

2. Improve Touch Responsiveness via Hardware Rendering
You can force the Android system to use GPU for rendering each 2d
frame in apps. Since Android uses frame by frame rendering of the
screen normally, the following code will offload the rendering to
GPU by a vast amount. Moreover, it will increase processing,
provide better RAM management and make the experience smoother.

    debug.sf.hw=1
    persist.sys.ui.hw=1
    debug.performance.tuning=1
    video.accelerate.hw=1
    debug.egl.profiler=1
    debug.egl.hw=1
    debug.composition.type=gpu

1. Stream Videos Faster
Android uses the media framework called “Stagefright”. Although
Stagefright is more open and simple, it is often buggy compared
to the old OpenCore framework. However, developers have greatly
improved its stability. The new framework can be altered to
result in faster streaming of online videos, but this might
affect the playback stability in some devices. If it’s ruining
your experience, revert to the original values.

    media.stagefright.enable-player=true
    media.stagefright.enable-meta=true
    media.stagefright.enable-scan=true
    media.stagefright.enable-http=true
    media.stagefright.enable-rtsp=true
    media.stagefright.enable-record=true
