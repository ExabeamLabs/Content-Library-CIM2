#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-login-fail-userloginfailed
  ParserVersion = v1.0.0
  Product = Microsoft 365
  Conditions = [ """destinationServiceName =Office 365""", """"Operation":"UserLoginFailed"""", """"ResultStatus":""", """"ClientIP":"""  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-o365-app-login-2.Fields} [
    """"ResultStatusDetail":"((?i)Success|({failure_reason}[^"]+))"""",
    """"LogonError":"({failure_reason}[^"]+)""",
    """"Operation":"UserLogin({result}[^"]+)""",
    """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
    """"ErrorNumber":"({error_code}\d+)"""",
    """reason=({failure_code}[^=]+?)\s\w+=""",
    """"OS.*?Value":"({os}[^"]+)"""",
    """"BrowserType.*?Value":"({browser}[^"]+)""""
  ]

cef-o365-app-login-2 = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """"UserId":"({email_address}[^@\s"]+@[^@\s\."]+\.[^\s",]+)"""",
    """"ClientIP":"\[?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(\]:({src_port}\d+))?"""",
    """"Operation":"({event_name}[^"]+)""",
    """"ResultStatus":"({result}[^"]+)"""",
    """destinationServiceName =({app}Office 365)""",
    """"Name":"UserAgent","Value":"({user_agent}[^"]+?)\s*""""
    
}
```