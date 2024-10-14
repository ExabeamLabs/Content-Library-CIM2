#### Parser Content
```Java
{
Name = "netmotionwireless-nw-kv-vpn-logout-success-disconnect"
Vendor = "NetMotion Wireless"
Product = "NetMotion Wireless"
TimeFormat = "epoch"
Conditions = [
"""Disconnect"""
"""Log_Date_Time"""
]
Fields = [
"""Log_Date_Time=({time}\d{13})"""
"""Device_Name ="+({src_host}[^\"]+)"""
"""User_Name ="+([^\\]+\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```