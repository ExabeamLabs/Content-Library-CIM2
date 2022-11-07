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
    """\ssrc=({src_ip}[^\s]+)""",
    """dhost=({dest_host}[^\s]+)""",
    """ext__proto=({protocol}.+?)\s\w+=""",
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```