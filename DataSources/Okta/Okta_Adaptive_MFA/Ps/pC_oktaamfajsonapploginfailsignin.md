#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-fail-signin
  Conditions = [ """"message"":""Sign-in Failed""", """"published"":""""" ]
  Fields = ${OktaParserTemplates.q-okta-app-login.Fields}[
    """Sign-in Failed\s*-\s*({failure_reason}[^"]+?)""""
  ]
  ParserVersion = "v1.0.0"

q-okta-app-login = {
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"published"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"message"+:"+({event_name}.+?)\s*(\.|\[|")""",
    """"ipAddress"+:"+({src_ip}[a-fA-F\d.:]+)""",
    """"displayName"+:"+((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))",[^\{\}]*?"objectType"+:"+User"""",
    """"login"+:"+({email_address}[^"@]+@({email_domain}[^"@]+))[^\{\}]*?"objectType"+:"+User"""",
    """"id"+:"+({user_agent}[^"]+)",[^\{\}]*?"objectType"+:"+Client"""",
    """({app}Okta)""",
    """"displayName"+:"+({app}[^"]+)",[^\{\}]*?"objectType"+:"+AppInstance"""",
    """"categories.*?objectType"+:"+({operation}[^"]+)"""",
  
}
```