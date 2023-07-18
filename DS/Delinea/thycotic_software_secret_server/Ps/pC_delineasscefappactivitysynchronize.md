#### Parser Content
```Java
{
Name = delinea-ss-cef-app-activity-synchronize
  Vendor = Delinea
  Product = Thycotic Software Secret Server
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [
    """CEF:0|Thycotic Software|Secret Server|""",
    """|DOMAIN - SYNCHRONIZE|2|"""
  ]
  Fields = [
    """rt=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """msg=({operation}.+?)\s+\w+=""",
    """\ssuser=([^\\\s]+?\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```