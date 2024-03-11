#### Parser Content
```Java
{
Name = okta-mfa-json-app-logout-success-published
Vendor = Okta
Product = Okta Adaptive MFA
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """"message"":""Sign-out successful""", """"published"":""""" ]
Fields = [
""""published"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
""""message"+:"+({event_name}.+?)\s*(\.|\[|")""",
""""ipAddress"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
""""displayName"+:"+({full_name}[^"]+)",[^\{\}]*?"objectType"+:"+User"""",
""""login"+:"+({email_address}[^"@]+@[^"@]+)[^\{\}]*?"objectType"+:"+User"""",
""""id"+:"+({user_agent}[^"]+)",[^\{\}]*?"objectType"+:"+Client"""",
""""displayName"+:"+(UNKNOWN|({browser}[^"]+))",[^\{\}]*?"objectType"+:"+Client"""",
"""({app}Okta)""",
""""displayName"+:"+({app}[^"]+)",[^\{\}]*?"objectType"+:"+AppInstance"""",
]


}
```