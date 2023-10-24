#### Parser Content
```Java
{
Name = extremenetworks-zwlanm-str-endpoint-notification-success-filesystem
 Vendor = Extreme Networks
 Product = Zebra WLAN Management
 ParserVersion = v1.0.0
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
 Conditions = [ """%25DIAG-4-FREE_RAM_DISK:""", """Free system:""" ]
 Fields =[
    """({time}\d+-\d+-\d+T\d+:\d+:\d+).\d[^\s]+\s+({host}[^\s]+)\s+({event_name}[^:]+):\s+({additional_info}[^"]+?)\s*"*$"""   
 ]


}
```