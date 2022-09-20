#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-login-fail-userloginfailed
  ParserVersion = v1.0.0
  Product = Office 365
  Conditions = [ """destinationServiceName =Office 365""", """"Operation":"UserLoginFailed"""", """"ResultStatus":""", """"ClientIP":"""  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-o365-app-login-2.Fields} [
    """"ResultStatusDetail":"((?i)Success|({failure_reason}[^"]+))"""",
    """"LogonError":"({failure_reason}[^"]+)""",
  ]

cef-o365-app-login-2 = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """"UserId":"({email_address}[^@\s"]+@[^@\s\."]+\.[^\s",]+)"""",
    """"ClientIP":"\[?({src_ip}[A-Fa-f:\d.]+?)(\]:({src_port}\d+))?"""",
    """"Operation":"({event_name}[^"]+)""",
    """"ResultStatus":"({result}[^"]+)"""",
    """destinationServiceName =({app}Office 365)""",
    """"Name":"UserAgent","Value":"({user_agent}[^"]+?)\s*""""
    
}
```