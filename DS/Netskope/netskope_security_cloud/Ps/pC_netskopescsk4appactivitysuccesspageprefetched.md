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
    """"timestamp":\s*({time}\d{10})""",
    """requestClientApplication=({app}[^=]+?)\s+(\w+=|$)""",
    """"app":\s*"\[?({app}[^"\]]+)""",
    """"srcip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"object":\s*"(\s+"|(\s*(Unknown Unknown|unknown|Unknown|null|({object}[^"]+?))\s*"))""",
    """"user":\s*"(unknown|(({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)|(({domain}[^\s"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[^\s"@\\\/]+))))"""",
    """\Wsuid=(?!\S+@\S+)({user}[^\s@]+)\s*(\w+=|$)"""
    """"activity":\s*"({operation}[^"]+)"""",
    """msg=({additional_info}[^=\.]+)""",
    """"page":"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?)"""",
    """"page":"(\w+:\/\/)?({web_domain}[^\\\/"]+)"""
  ]


}
```