#### Parser Content
```Java
{
Name = cloudfare-waf-sk4-alert-trigger-success-firewall
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CEF:""", """destinationServiceName =cloudflare""",""""kind":"firewall""""]
  Fields = [
    """ext__occurred_at_=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """suser=({user}.+?)\s\w+=""",
    """shost=({host}[^\s]+)""",
    """act=({alert_type}.+?)\s\w+=""",
    """cat=({alert_name}.+?)\s\w+=""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dhost=({dest_host}[^\s]+)""",
    """ext__proto=({protocol}.+?)\s\w+=""",
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```