#### Parser Content
```Java
{
Name = "delinea-ss-cef-app-start-systemlog"
  Vendor = "Delinea"
  Product = "Thycotic Software Secret Server"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
    """CEF:0|Thycotic Software|Secret Server|"""
    """|System Log|3|"""
  ]
  Fields = [
    """rt=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
    """msg=({operation}.+?) rt="""
  ]
  ParserVersion = "v1.0.0"


}
```