#### Parser Content
```Java
{
Name = shibboleth-s-str-user-password-modify-success-passwordchange
  ParserVersion = v1.0.0
  Vendor = Shibboleth
  Product = Shibboleth
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """password change from""", """SUCCESS""" ]
  Fields = [ 
    """\] ({user}[\w\.\-]{1,40}\$?)\s+password change from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```