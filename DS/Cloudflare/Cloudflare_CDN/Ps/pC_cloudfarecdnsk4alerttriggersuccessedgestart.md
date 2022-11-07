#### Parser Content
```Java
{
Name = cloudfare-cdn-sk4-alert-trigger-success-edgestart
  Vendor = Cloudflare
  Product = Cloudflare CDN
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """destinationServiceName =cloudflare""", """"actor":""" ]
  Fields = [
    """suser=({user}.+?)\s\w+=""",
    """act=({alert_type}.+?)\s\w+=""",
    """cat=({alert_name}.+?)\s\w+=""", 
    """\ssrc=({src_ip}[^\s]+)""",
    """dst=({dest_ip}[^\s]+)""",
    """dhost=({dest_host}[^\s]+)""",
    """proto=({protocol}.+?)\s\w+=""",
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```