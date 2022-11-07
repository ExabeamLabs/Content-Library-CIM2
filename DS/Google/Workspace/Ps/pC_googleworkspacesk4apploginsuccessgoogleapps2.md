#### Parser Content
```Java
{
Name = google-workspace-sk4-app-login-success-googleapps2
  Vendor = Google
  Product = Workspace
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =Google Apps""", """|login-success|""", """cs6=""" ]
  Fields = [
    """"time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"ipAddress"\s*:\s*"({src_ip}[\da-fA-F\.:]+)"""",
    """({operation}login-success)""",
    """({event_name}login_success)""",
    """"profileId"\s*:\s*"({user_id}\d+)""",
    """"actor"\s*:\s*\{[^\}]*?"email"\s*:\s*"({email_address}({user}[^@"]+)@[^"]+)"""",
    """"events"[\\n\s]*:[^\]]*?"name"[\\n\s]*:[\\n\s]*"login_type"[\\n\s]*,[\\n\s]*"value"[\\n\s]*:[\\n\s]*"({login_type_text}[^"]+?)"""",
    """({app}Google Apps)"""
  ]


}
```