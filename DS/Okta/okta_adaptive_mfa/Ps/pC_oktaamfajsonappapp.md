#### Parser Content
```Java
{
Name = okta-amfa-json-app-app
Vendor = Okta
Product = Okta Adaptive MFA
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """objectType": "app."""
  """"actors":"""
]
Fields = [
  """"published":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """"ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """targets.+?login":\s*"(({email_address}[^"\s@]+@({domain}[^"\s@,]+))|({user}[^"\s,@]+))"""
  """AppInstance[^\}\{]+displayName":\s*"({app}[^"]+)""""
  """\{.+?displayName":\s*"({app}[^"]+)"[^\}\{]+AppInstance"""
  """"objectType":\s*"app\.({operation}[^"]+)""""
  """categories":\s*\["({operation}[^,"]+)"""
  """message":\s*"({additional_info}[^"]+?)\s*""""
  """"id":\s*"({user_agent}[^"]+)([^\}\{]+"Client")"""
  """(Client"[^\}\{]+)"id":\s*"({user_agent}[^"]+)"""
  """requestUri":\s*"({request_uri}[^"]+?)\s*""""
]
ParserVersion = "v1.0.0"


}
```