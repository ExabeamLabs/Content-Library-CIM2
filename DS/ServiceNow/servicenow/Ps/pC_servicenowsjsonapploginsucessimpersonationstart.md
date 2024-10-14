#### Parser Content
```Java
{
Name = servicenow-s-json-app-login-sucess-impersonationstart
  ParserVersion = v1.0.0
  Conditions = [ """"instance":""", """"name":"impersonation.start"""", """"sys_created_on":""", """"sys_created_by":""" ]

servicenow-login-template = {
    Vendor = ServiceNow
    Product = ServiceNow
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """"sys_created_on":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """({app}ServiceNow)""",
      """"user(_name)?":"((?i)(anonymous)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"\s@]+)|({=user}[^"\s@]+))"""",
      """"name":"({object}[^"]+)""",
      """"name":"({event_name}[^"]+)"""",
      """"queue":"({event_name}[^"]+)""",
      """"parm1":"\s*(|-|({resource}[^",]+?[^\\\s])\s*)",""",
      """"parm2":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    
}
```