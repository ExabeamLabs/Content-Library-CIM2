#### Parser Content
```Java
{
Name = "delinea-ss-cef-endpoint-scan-wmifailed"
  Vendor = "Delinea"
  Product = "Secret Server"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
    """CEF:0|Thycotic Software|Secret Server|"""
    """Windows Service scan with WMI FAILED"""
  ]
  Fields = [
    """rt=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
    """ Computer: ({host}[\w\-.]+?) with user"""
    """user: (({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?) """
    """msg=({additional_info}.+?) rt="""
  ]
  ParserVersion = "v1.0.0"


}
```