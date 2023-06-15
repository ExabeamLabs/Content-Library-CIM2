#### Parser Content
```Java
{
Name = oracle-am-str-app-login-success-auth
  Vendor = Oracle
  Product = Oracle Access Management
  TimeFormat = "MM/dd/yyyy HH:mm:ss Z"
  Conditions = [ """- AUTH""", """_SUCCESS -""", """- 2uid=""" ]
  Fields = [
    """({time}\d\d\\\/\d\d\\\/\d\d\d\d \d\d:\d\d:\d\d \\(-|\+)\d\d\d\d)\s+-\s*({subtype}.*?)\s+-\s*({method}.*?)\s+-\s*({host}.*?)\s+-\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+-\s*({app}.*?)\s+-\s*({ldap}.*?)\s+-\s*({clock}.*?)\s+-\s*({protocol}.*?)\s+-\s*({dest_host}.*?)\s+-"""
    """- 2uid=({user}[^\s]+)""" 
  ]
  ParserVersion = v1.0.0


}
```