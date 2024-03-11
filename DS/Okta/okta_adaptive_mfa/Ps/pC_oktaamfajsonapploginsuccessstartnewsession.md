#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-success-startnewsession
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Start New Session""", """"tenantHost":""" ]
  Fields = [
    """"userAgent":\s*"({user_agent}[^"]+)""",
    """"requestTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"deviceType":\s*"(login_type)""",
    """"systemAccount":\s*";*({user}[^;"]+)""",
    """"tenantHost":\s*"({app}[^"]+)""",
    """"activityAction":\s*"({operation}[^"]+)""",
    """"ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"target":\s*\{[^\}]*"descriptor":\s*"({user}[^\/"]+?)\s*\/\s*({full_name}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```