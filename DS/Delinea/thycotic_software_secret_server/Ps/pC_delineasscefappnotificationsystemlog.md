#### Parser Content
```Java
{
Name = "delinea-ss-cef-app-notification-systemlog"
  Vendor = "Delinea"
  Product = "Thycotic Software Secret Server"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
    """CEF:0|Thycotic Software|Secret Server|"""
    """|System Log|7|"""
  ]
  Fields = [
    """rt=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
    """msg=({additional_info}.+?) rt="""
  ]
  ParserVersion = "v1.0.0"


}
```