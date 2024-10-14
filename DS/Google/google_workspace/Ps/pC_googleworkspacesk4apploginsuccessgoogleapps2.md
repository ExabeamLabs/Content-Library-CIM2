#### Parser Content
```Java
{
Name = google-workspace-sk4-app-login-success-googleapps2
  Vendor = Google
  Product = Google Workspace
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =Google Apps""", """|login-success|""", """cs6=""" ]
  Fields = [
    """"time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"ipAddress"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """({operation}login-success)""",
    """({event_name}login_success)""",
    """"profileId"\s*:\s*"({user_id}\d+)""",
    """suser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+[\w=]+""",
    """"actor"\s*:\s*\{[^=]*?"email"\s*:\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"events"[\\n\s]*:[^\]]*?"name"[\\n\s]*:[\\n\s]*"login_type"[\\n\s]*,[\\n\s]*"value"[\\n\s]*:[\\n\s]*"({login_type_text}[^"]+?)"""",
    """({app}Google Apps)"""
  ]


}
```