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
    """"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"login":"({email_address}[^"@]+@({email_domain}[^@"]+))""",
    """"event_type":"({event_name}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```