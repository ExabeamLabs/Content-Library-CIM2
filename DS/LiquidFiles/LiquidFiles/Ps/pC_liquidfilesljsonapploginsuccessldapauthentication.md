#### Parser Content
```Java
{
Name = liquidfiles-l-json-app-login-success-ldapauthentication
    Vendor = LiquidFiles
    Product = LiquidFiles
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
	Conditions = [ """liquidfiles[""", """"message":"LDAP Authentication Successful"""" ,""""ldap_user_name":""",""""ldap_user_email":""" ]
    Fields = [
      """"hostname":"({host}[^"]+)"""",
      """"filename":"({file_name}[^"]+(\.)({file_ext}[^"]+))"""",
      """"ip":"({src_ip}[A-Fa-f\d:.]+)"""",
      """"user_id":"(n/a|({user}[^"]+?))"""",
      """"message":"({event_name}[^:"]+)""",
      """({app}liquidfiles)""",
      """"username":"(({email_address}[^@"]+@[^\.]+\.[^"]+)|({user}[^"]+))"""",
    ]
	ParserVersion = v1.0.0
  

}
```