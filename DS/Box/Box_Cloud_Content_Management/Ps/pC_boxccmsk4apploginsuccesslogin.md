#### Parser Content
```Java
{
Name = box-ccm-sk4-app-login-success-login
  Vendor = Box
  Product = Box Cloud Content Management
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """destinationServiceName =Box""", """cs6=""", """"event_type":"LOGIN"""" ]
  Fields = [
    """({app}Box)""",
    """({operation}login-success)""",
    """"created_at":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\Wdproc=({process_name}[^=]+?)(\s+\w+=|\s*$)""",
    """"ip_address":"({src_ip}[\da-fA-F.:]+)"""",
    """"login":"({email_address}[^"@]+@({email_domain}[^@"]+))""",
    """"event_type":"({event_name}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```