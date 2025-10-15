#### Parser Content
```Java
{
Name = "unix-unix-str-app-notification-success-dkimsignatureadded"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["MMM dd HH:mm:ss"]
  Conditions = [ 
    """DKIM-Signature"""
    """opendkim["""
  ]
  Fields = [
    """({time}\w\w\w \d\d \d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s({process_name}[^\[]+)\[({process_id}[^\]]+)]:\s*\w+:\s*({additional_info}[^$]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```