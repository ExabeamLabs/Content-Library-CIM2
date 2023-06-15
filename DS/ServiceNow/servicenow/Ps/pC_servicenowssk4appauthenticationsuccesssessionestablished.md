#### Parser Content
```Java
{
Name = servicenow-s-sk4-app-authentication-success-sessionestablished
  Vendor = ServiceNow
  ParserVersion = "v1.0.0"
  Product = ServiceNow
  Conditions = [ """destinationServiceName =ServiceNow""", """"name":"session.established"""" ]
  Fields = ${ServiceNowParsersTemplates.servicenow-auth-template.Fields}[
    """"parm2":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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