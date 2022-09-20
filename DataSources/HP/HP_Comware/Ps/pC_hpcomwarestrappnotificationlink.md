#### Parser Content
```Java
{
Name = hp-comware-str-app-notification-link
    ParserVersion = "v1.0.0"
    Vendor = HP
    Product = HP Comware
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = ["""LINK_UPDOWN"""]
    Fields = [
      """link\sstatus\sis\s([^.]+)""",
# link_status is removed
    ]
  

}
```