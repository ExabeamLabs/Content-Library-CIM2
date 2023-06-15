#### Parser Content
```Java
{
Name = servicenow-s-sk4-app-logout-success-logout
  Vendor = ServiceNow
  ParserVersion = "v1.0.0"
  Product = ServiceNow
  Conditions = [ """destinationServiceName =ServiceNow""", """"name":"logout"""" ]
  Fields = ${ServiceNowParsersTemplates.servicenow-auth-template.Fields}[
    """"parm2":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]

servicenow-auth-template = {
    Vendor = ServiceNow
    Product = ServiceNow
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """"sys_created_on":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """destinationServiceName =({app}ServiceNow)""",
      """"user(_name)?":"(({email_address}[^@"]+@[^.]+\.[^"]+)|({user}[^",]+))"""
      """"name":"({object}[^"]+)""",
      """"parm1":"\s*(|-|({resource}[^",]+?[^\\\s])\s*)","""
    
}
```