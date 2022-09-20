#### Parser Content
```Java
{
Name = servicenow-s-json-app-login-sucess-impersonationstart
  ParserVersion = v1.0.0
  Conditions = [ """destinationServiceName =ServiceNow""", """"name":"impersonation.start"""" ]

servicenow-login-template = {
    Vendor = ServiceNow
    Product = ServiceNow
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """"sys_created_on":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """({app}ServiceNow)""",
      """"user(_name)?":"((?i)(anonymous)|({user}[^"\s@]+)@({domain}[^"\s@]+)|({=user}[^"\s@]+))"""",
      """"name":"({object}[^"]+)""",
      """"name":"({event_name}[^"]+)"""",
      """"queue":"({event_name}[^"]+)""",
      """"parm1":"\s*(|-|({resource}[^",]+?[^\\\s])\s*)",""",
      """"parm2":"({src_ip}[A-Fa-f\d:.]+)"""",
    
}
```