#### Parser Content
```Java
{
Name = servicenow-s-sk4-app-logout-success-impersonationend
  Vendor = ServiceNow
  ParserVersion = "v1.0.0"
  Product = ServiceNow
  Conditions = [ """destinationServiceName =ServiceNow""", """"name":"impersonation.end"""" ]

servicenow-auth-template = {
    Vendor = ServiceNow
    Product = ServiceNow
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """"sys_created_on":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """destinationServiceName =({app}ServiceNow)""",
      """"user(_name)?":"(({email_address}[^@"]+@[^.]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      """"name":"({object}[^"]+)""",
      """"parm1":"\s*(|-|({resource}[^",]+?[^\\\s])\s*)","""
    
}
```