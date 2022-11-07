#### Parser Content
```Java
{
Name = oracle-am-str-app-login-success-auth
  Vendor = Oracle
  Product = Access Manager
  TimeFormat = "MM\\/dd\\/yyyy HH:mm:ss \\Z"
  Conditions = [ """- AUTH""", """_SUCCESS -""", """- 2uid=""" ]
  Fields = [
    """({time}\d\d\\\/\d\d\\\/\d\d\d\d \d\d:\d\d:\d\d \\(-|\+)\d\d\d\d)\s+-\s*({subtype}.*?)\s+-\s*({method}.*?)\s+-\s*({host}.*?)\s+-\s*({dest_ip}.*?)\s+-\s*({app}.*?)\s+-\s*({ldap}.*?)\s+-\s*({clock}.*?)\s+-\s*({protocol}.*?)\s+-\s*({src_host}.*?)\s+-"""   
    """- 2uid=({user}[^\s]+)""" 
  ]
  ParserVersion = v1.0.0


}
```