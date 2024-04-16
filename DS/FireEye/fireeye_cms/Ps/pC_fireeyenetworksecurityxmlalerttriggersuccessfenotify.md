#### Parser Content
```Java
{
Name = fireeye-networksecurity-xml-alert-trigger-success-fenotify
  Vendor = FireEye
  Product = FireEye CMS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """fenotify-""","""<src vlan=""" ]
  Fields = [
    """<occurred>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """ fenotify-({alert_id}\d+)""",
    """<src vlan=\".+\">\s*<ip>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<src .+?<host>({src_host}[^<]+)""",
    """<dst>.+?<ip>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?</ip""" 
  ]
  ParserVersion = "v1.0.0"


}
```