#### Parser Content
```Java
{
Name = juniper-srx-str-app-authentication-success-authsuccessfor
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """NetScreen""", """ device_id=""", """authentication successful for""" ]
  Fields = [
    """\Wdevice_id=({host}[\w\-.]+)\s+""",# severity_level is removed
    """\(({time}\d\d\d\d-\d\d-\d\d \d\d\:\d\d:\d\d)\)""",
    """authentication successful for (admin user|login name)\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """authentication successful for (admin user|login name)\s+'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """authentication successful for.+?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    
  ]
  ParserVersion = "v1.0.0"


}
```