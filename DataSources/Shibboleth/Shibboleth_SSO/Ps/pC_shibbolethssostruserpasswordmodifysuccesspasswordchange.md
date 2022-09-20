#### Parser Content
```Java
{
Name = shibboleth-sso-str-user-password-modify-success-passwordchange
  ParserVersion = v1.0.0
  Vendor = Shibboleth
  Product = Shibboleth SSO
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """password change from""", """SUCCESS""" ]
  Fields = [ 
    """\] ({user}.+?)\s+password change from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  ]


}
```