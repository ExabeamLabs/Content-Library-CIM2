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
"""({device_id}USB[^"]+)",\d+,"({dest_host}[^"]+)","*({user}[^",]+)"*,"*({file_name}[^"]+)"*,"*({bytes}\d+)"*,\d+,"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
]
ParserVersion = "v1.0.0"


}
```