#### Parser Content
```Java
{
Name = netskope-sc-sk4-app-activity-success-pageprefetched
  ParserVersion = v1.0.0
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [ """"type":"""", """destinationServiceName =Netskope""", """"activity":""""]
  Fields = [
    """"timestamp":\s*({time}\d+)""",
    """requestClientApplication=({app}[^=]+?)\s+(\w+=|$)""",
    """"app":\s*"\[?({app}[^"\]]+)""",
    """"srcip":\s*"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """"object":\s*"(\s+"|(\s*(Unknown Unknown|unknown|Unknown|null|({object}[^"]+?))\s*"))""",
    """"user":\s*"(unknown|(({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)|(({domain}[^\s"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[^\s"@\\\/]+))))"""",
    """"activity":\s*"({operation}[^"]+)"""",
    """msg=({additional_info}[^=\.]+)""",
  ]


}
```