#### Parser Content
```Java
{
Name = hp-comware-str-app-notification-link
    ParserVersion = "v1.0.0"
    Vendor = HP
    Product = HPE Comware
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = ["""LINK_UPDOWN"""]
    Fields = [
      """link\sstatus\sis\s([^.]+)""",
      """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)"""
# link_status is removed
    ]


}
```