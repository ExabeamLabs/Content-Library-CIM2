#### Parser Content
```Java
{
Name = "unix-unix-str-app-notification-success-consul"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["MMM dd HH:mm:ss"]
  Conditions = [ 
    """consul["""
    """]:"""
  ]
  Fields = [
    """({time}\w\w\w \d\d \d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s({process_name}[^\[]+)\[({process_id}[^\]]+)]:.*?[^\d]:\s*({additional_info}[^$]+)"""
    """error="({error_info}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```