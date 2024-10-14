#### Parser Content
```Java
{
Name = "usb-u-csv-peripheral-storage-activity-success-activity"
Vendor = "USB"
Product = "USB"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""cs:usb:activity"""
""""USB"""
]
Fields = [
"""({device_id}USB[^"]+)",\d+,"({dest_host}[^"]+)","*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"*,"*({file_name}[^"]+)"*,"*({bytes}\d+)"*,"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
"""VID_({device_vid}[^&]+)&(amp;)?PID_({device_pid}[^\\&]+)"""
]
ParserVersion = "v1.0.0"


}
```