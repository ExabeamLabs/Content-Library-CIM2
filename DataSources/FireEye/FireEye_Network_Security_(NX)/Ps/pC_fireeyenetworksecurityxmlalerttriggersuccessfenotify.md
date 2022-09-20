#### Parser Content
```Java
{
Name = fireeye-networksecurity-xml-alert-trigger-success-fenotify
  Vendor = FireEye
  Product = FireEye Network Security (NX)
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """fenotify-""","""<src vlan=""" ]
  Fields = [
    """<occurred>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """ fenotify-({alert_id}\d+)""",
    """<src vlan=\".+\">\s*<ip>({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """<src .+?<host>({src_host}[^<]+)""",
    """<dst>.+?<ip>({dest_ip}[^<]+)</ip""" 
  ]
  ParserVersion = "v1.0.0"


}
```