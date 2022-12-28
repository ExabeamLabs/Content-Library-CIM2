#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-success-singlesignon
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"message"":""User performed single sign on to app""", """"published"":""""" ]
  Fields = [
    """"published"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"message"+:"+({event_name}.+?)\s*(\.|\[|")""",
    """"ipAddress"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"displayName"+:"+((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))",[^\{\}]*?"objectType"+:"+User"""",
    """"login"+:"+({email_address}[^"@]+@({email_domain}[^"@]+))[^\{\}]*?"objectType"+:"+User"""",
    """"id"+:"+({user_agent}[^"]+)",[^\{\}]*?"objectType"+:"+Client"""",
    """({app}Okta)""",
    """"displayName"+:"+({app}[^"]+)",[^\{\}]*?"objectType"+:"+AppInstance"""",
    """"categories.*?objectType"+:"+({operation}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```