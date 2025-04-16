#### Parser Content
```Java
{
Name = "delinea-ss-cef-app-start-systemlog"
  Vendor = "Delinea"
  Product = "Secret Server"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
    """CEF:0|Thycotic Software|Secret Server|"""
    """|System Log|3|"""
  ]
  Fields = [
    """rt=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
    """msg=({additional_info}.+?) rt="""
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```