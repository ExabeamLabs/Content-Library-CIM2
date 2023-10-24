#### Parser Content
```Java
{
Name = "okta-amfa-json-app-login-fail-signinfailure"
 Vendor = "Okta"
 Product = "Okta Adaptive MFA"
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 Conditions = [
   """Sign-in Failure"""
   """"published":"""
 ]
 Fields = [
   """"published":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
   """"ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
   """"login":\s*"({email_address}[^"@]+@({domain}[^"@]+))"""
   """"login":\s*"({user}[\w\.\-]{1,40}\$?)""""
   """Sign-(I|i)n Failed\s*-\s*({failure_reason}[^"]+)""""
   """AppInstance[^\}\{]+displayName":\s*"({app}[^"]+)""""
   """\{.+?displayName":\s*"({app}[^"]+)"[^\}\{]+AppInstance"""
   """targets":\s*\[\{"displayName":\s*"({app}[^"]+)""""
   """"id":\s*"({user_agent}[^"]+)([^\}\{]+"Client")"""
 ]
 ParserVersion = "v1.0.0"


}
```