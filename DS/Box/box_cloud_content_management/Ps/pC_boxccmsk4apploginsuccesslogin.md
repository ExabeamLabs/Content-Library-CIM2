#### Parser Content
```Java
{
Name = box-ccm-sk4-app-login-success-login
  Vendor = Box
  Product = Box Cloud Content Management
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "EEE MMM dd HH:mm:ss zzz yyyy"]
  Conditions = [ """destinationServiceName =Box""", """cs6=""", """"event_type":"LOGIN"""" ]
  Fields = [
    """({app}Box)""",
    """({operation}login-success)""",
    """"created_at":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"created_at":"({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \w+ \d+)""""
    """\Wdproc=({process_name}[^=]+?)(\s+\w+=|\s*$)""",
    """"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"event_type":"({event_name}[^"]+)"""
    """created_by"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+({full_name}[^":,]+)[",\]\}]""",
    """created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]
  ParserVersion = "v1.0.0"


}
```