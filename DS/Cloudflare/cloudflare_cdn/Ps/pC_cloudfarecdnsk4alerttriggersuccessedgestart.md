#### Parser Content
```Java
{
Name = cloudfare-cdn-sk4-alert-trigger-success-edgestart
  Vendor = Cloudflare
  Product = Cloudflare CDN
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """destinationServiceName =cloudflare""", """"actor":""" ]
  Fields = [
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
    """act=({alert_type}.+?)\s\w+=""",
    """cat=({alert_name}.+?)\s\w+=""", 
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """dhost=({dest_host}[^\s]+)""",
    """proto=({protocol}.+?)\s\w+=""",
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```