#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-auditevent
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =Office 365""", """"description":"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """destinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
    """"description":"({additional_info}[^"]+)""",
    """category":"({category}[^"]+)"""",
    """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """"operationName":"({operation}[^"]+)""",
    """action":"({action}[^"]+)""",
    """"((?i)callerIpAddress|CIp)":"({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))(:({src_port}\d+))?"""",
    """"email":"({email_address}[^\s@"]+@[^\s@"]+)""",
    """"userAgent":"({user_agent}[^"]+)"""",
    """"statusCode\\":({result_code}\d+)""",
    """userId":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))""",
    """\[Namespace:\s*({host}\S+) ; EventHub name:""",
    """"clientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"userName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """suser=((?i)anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"(?i)resourcename":"({resource}[^"]+)"""",
    """"(?i)resourcetype":"({resource_type}[^"]+)"""",
    """resource\s<b>({resource}[^<]+)<\/b>""",
    """device\s<b>({host}[^<]+)<\/b>""",
    """\suser\s<b>(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<\/b>"""
  ]
  ParserVersion = "v1.0.0"


}
```