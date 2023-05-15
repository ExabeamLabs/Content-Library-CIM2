#### Parser Content
```Java
{
Name = hp-hpilo-str-app-login-success-xmllogin
    ParserVersion = v1.0.0
    Vendor = HP
    Product = HP iLO
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """XML login: """, """ILO""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """\d\d:\d\d:\d\dZ\s({host}[^\s]+)\s\#ILO""",
      """({app}ILO)""",
      """\slogin:\s({user}[^\s]+)""",
      """\slogin:\s(\S+\s){2}({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\(({src_host}[^\)]+)\)"""
      """({event_name}XML login)"""
    ]
    DupFields = ["host->dest_host"]
  

}
```