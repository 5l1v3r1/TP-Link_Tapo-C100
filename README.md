 # TP-Link_Tapo-C100

- This repos is not done, repo will be updated now and when this text is gone this repo is complete.

![Screenshot_20221112_132759](https://user-images.githubusercontent.com/26827453/201473935-8cf90a72-37e8-4dd7-85f9-8e96a80e652a.png)

![Screenshot_20221112_132634](https://user-images.githubusercontent.com/26827453/201473951-3ac58a5f-322d-41c8-8f9b-8e59566e39bd.png)

# rtsp streams


* Play this stream using the URL:  rtsp://192.168.1.138/stream1
* Play this stream using the URL: rtsp://192.168.1.138/stream2

### Stream via mplayer

* mplayer is required to be built with rmp useflag

```bash
printf '%s' 'media-video/mplayer rtmp' >> /etc/portage/package.yuse
emerge --ask media-video/mplayer
```

### Stream current stream via mplayer

```
mplayer rtsp://192.168.1.138/stream1
```

```
# ul < tmp/base-files/etc/dn_switch.ini
C100 1.0:smartir_enable
C100 1.0:smartir_level
name=C100 1.0
led_cnt=1
with_ldr=0
irt_comm[0]={143,27}
irt_comm[1]={124,20}
irt_comm[2]={115,10}
irt_comm[3]={95,6}
irt_comm[4]={77,4}
irt_comm[5]={60,3}
irt_comm[6]={55,2}
irt_comm[7]={50,1}
ir_cut_day_gpio_num=9
ir_cut_night_gpio_num=11
ir_led_gpio_num=17
irt_ncomm={77,4}
ir_delay=5
gain_I={0.970000,0.980000}
gain_N={1.180000,1.670000}
natural_rate_thresh=0.050000
thresh_no_adc={1500,1200,900,630,440,160,60,20}
day_ae_compensation={0,0,0,0,0,0,0,0}
day_ae_antiflicker_enable=1
day_ae_antiflicker_freq=50
night_ae_compensation=0
night_ae_antiflicker_enable=0
day_drc_asymmetry={20,17,14,11,8,4,0,0}
night_drc_asymmetry={0,0,0,0,0,5,15,0}
ae_gain_level={0,2,4,8,16,32,64,128}
smartir_enable=0
smartir_level=30
day_auto_wdr_level=60
night_auto_wdr_level=60tmp/base-files/etc/dn_switch.ini
C100 1.0:smartir_enable
C100 1.0:smartir_level
name=C100 1.0
led_cnt=1
with_ldr=0
irt_comm[0]={143,27}
irt_comm[1]={124,20}
irt_comm[2]={115,10}
irt_comm[3]={95,6}
irt_comm[4]={77,4}
irt_comm[5]={60,3}
irt_comm[6]={55,2}
irt_comm[7]={50,1}
ir_cut_day_gpio_num=9
ir_cut_night_gpio_num=11
ir_led_gpio_num=17
irt_ncomm={77,4}
ir_delay=5
gain_I={0.970000,0.980000}
gain_N={1.180000,1.670000}
natural_rate_thresh=0.050000
thresh_no_adc={1500,1200,900,630,440,160,60,20}
day_ae_compensation={0,0,0,0,0,0,0,0}
day_ae_antiflicker_enable=1
day_ae_antiflicker_freq=50
night_ae_compensation=0
night_ae_antiflicker_enable=0
day_drc_asymmetry={20,17,14,11,8,4,0,0}
night_drc_asymmetry={0,0,0,0,0,5,15,0}
ae_gain_level={0,2,4,8,16,32,64,128}
smartir_enable=0
smartir_level=30
day_auto_wdr_level=60
night_auto_wdr_level=60
```


### mtd partiotions
```
[    0.405000] 0x000000000000-0x00000001d800 : "factory_boot"
[    0.434000] 0x00000001d800-0x000000020000 : "factory_info"
[    0.464000] 0x000000020000-0x000000040000 : "art"
[    0.474000] 0x000000040000-0x000000050000 : "config"
[    0.485000] 0x000000050000-0x000000060000 : "boot"
[    0.495000] 0x000000060000-0x0000001c6000 : "kernel"
[    0.521000] 0x0000001c6000-0x000000730000 : "rootfs"
[    0.549000] 0x000000730000-0x000000800000 : "rootfs_data"
[    0.561000] 0x000000060000-0x000000800000 : "firmware"
```
### Device Info

```
Board: IPCAM RTS3903 CPU: 500M :rx5281 prid=0xdc02
force spi nor mode
DRAM:  64 MiB @ 1066 MHz
flash status is 0, 0, 0
SF: Detected XM25QH64A with page size 256 Bytes, erase size 64 KiB, total 8 MiB
Flash: 0 Bytes
flash status is 0, 0, 0
SF: Detected XM25QH64A with page size 256 Bytes, erase size 64 KiB, total 8 MiB
Using default environment
```

### Boot Console Disable

```
[    0.262000] console [ttyS1] enabled, bootconsole disabled
[    0.262000] console [ttyS1] enabled, bootconsole disabled

```
### Linux Version

```
Linux version 3.10.27 (root@smartlifeci1) (gcc version 4.8.5 20150209 (prerelease) (Realtek RSDK-4.8.5p1 Build 2521) ) #1 PREEMPT Fri Oct 30 14:00:16 CST 2020
```

### Board

```
Board: IPCAM RTS3903 CPU: 500M :rx5281 prid=0xdc02
```

### Kernel Command Line

```
Kernel command line: console=ttyS1,57600 root=/dev/mtdblock6 rts-quadspi.channels=dual
```

### Hardware Info (cloud-service)

```bash
[INFO][cloud-service] hw_id:       16F34FC28E5C7CD4224xxxxxxxxxxxx
[INFO][cloud-service] dev_id:      802188F5CF0D12A5ED5588036C08C6xxxxxx
[INFO][cloud-service] dev_type:    SMART.IPCAMERA
[INFO][cloud-service] dev_model:   C100
[INFO][cloud-service] dev_alias:   Tapo_Camera_39F6
[INFO][cloud-service] dev_mac:     28EE52xxx
[INFO][cloud-service] dev_name:    C100
[INFO][cloud-service] hw_ver:      1.0
[INFO][cloud-service] w_ver:       1.0.17 Build 201030 Rel.50426n(4555)
[INFO][cloud-service] oem_id:      88BFB135F137AD2F4C7701B6661Dxxxxxxx
```


### Config Dump

```bash
**************************************************
********************config dump*******************
--------------------------------------------------

*********************

*********************

cloud-brd version:              :-rc04, build_time:20201030_134545
sef domain                      : n-deventry-dcipc.tplinkcloud.com
sef port                        : 443
cloud svr default port          : 443
lt port                          : 443
default valid time              : 172800
heartbeat interval              : 55000
request timeout                 : 5000
reconnect timewait max          : 128000
reconnect cachedsvr max times   : 5
reconnect defaultsvr max times  : 5
reconnect random time min       : 2000
reconnect random time max       : 128000
short connect interval          : 259200000
max message number              : 1000
max client number               : 20
service file                    : /etc/cloud-sdk/cloud_service.cfg
cer file                        : /etc/cloud-sdk/2048_newroot.cer
ssl verify CN                   : 
ssl verify time                 : 0
**************************************************
```

### Server Info
```
[ERROR][cloud-service] dev_token_is_valid(56): token->valid: 0
[ERROR][cloud-service] dev_token_is_valid(56): token->valid: 0
[INFO][cloud-service] dev_token_update(138):    
****SERVER INFO****
                url:https://n-euw1-device-api.tplinkcloud.com
                protocol:HTTPS
                host:n-euw1-device-api.tplinkcloud.com
                port:443
 ```
 
### Auth
 ```

[INFO]Not found SD card, so will not start logrecord.
[INFO][cet][http_connection_new]-3386: New http connection fd: 25, point: 0x6f5ff8
[INFO][cet][http_header_add_encrypt]-814: Key-Exchange: cipher="AES_128_CBC" username="admin" padding="PKCS7_16" algorithm="MD5" nonce="df0932ea3149a633a30ff0cf3cb25d2b000001xxxxxx"
[INFO][cet][http_header_add_encrypt]-814: Key-Exchange: cipher="AES_128_CBC" username="admin" padding="PKCS7_16" algorithm="MD5" nonce="fd5b5809018f062a7ff97a02ff75469e000002xxxxxx"
[INFO][cet][http_stream_video_h264_mixed_cb]-736: digest auth success remote:0
[INFO][cet][generate_new_session_id]-110: Create new session (id: 7) in new http connection (fd: 25, point: 0x6f5ff8)
```
 
 ### Cloud Failure
 
 ```
 [2020-10-30 06:59:54][ERROR][cloud-sdk]cloud_ip_list.c:61:cloud_ip_list_parse-- get addr info error, host:n-deventry-dcipc.tplinkcloud.com, serv:443, Name or service not known
[2020-10-30 06:59:54][ERROR][cloud-sdk]cloud_session.c:1364:cloud_session_connect_sef-- fail to parse the SEF domain:n-deventry-dcipc.tplinkcloud.com:443
[2020-10-30 06:59:54][ERROR][cloud-sdk]cloud_session.c:362:cloud_session_active_long_time-- fail to connect the SEF, result:-1
----------ip changed from 192.168.0.10 to 192.168.1.137--------
----------router changed from 192.168.0.1 to 192.168.1.1--------
get dns form static dhcp:192.168.1.1, prev_append_dns:0.0.0.0
get new dns ip, reset append_dns as:192.168.1.1
[ERROR][relayd]cookie.c:544(cookies_init_conn_req) : failed when resolving hostname(aps1-relay-dcipc.i.tplinknbu.com).
[  276.058000] Erase from 0X40000 to 0X50000:
[  276.073000] .
[  276.081000] Program from 0X40000 to 0X50000:
```
 
