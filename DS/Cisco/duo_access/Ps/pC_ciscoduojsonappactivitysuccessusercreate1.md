#### Parser Content
```Java
{
Name = cisco-duo-json-app-activity-success-usercreate-1
  Product = Duo Access
  Conditions = [ """action=user_create;""", """object=""", """timestamp=""" ]
  ParserVersion = "v1.0.0"

q-duo-app-activity = {
  Vendor = Cisco
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Fields = [
    """\d\d:\d\d\s+({host}.+?)\s+(\S+\s+)*@\{action=({operation}[^;]+)""",
    """username=(?![^:]+:\s*[^;\}]+)({full_name}[^;\}]+)""",
    """"uname"+:\s*"{1,2}({user}[^"]+?)"+,""",
    """"realname"+:\s*"{1,2}({full_name}[^"]+?)"+,""",
    """object=\s*({object}[^;]+?)(?:;|\})""",
    """timestamp=\s*({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)""",
    """"email"+:\s*"{1,2}({email_address}[^@]+@({email_domain}[^"]+?))"+,""",
    """"ip_address"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"primary_auth_method"+:\s*"{1,2}({auth_method}[^"]+?)"+,""",
    """"factor"+:\s*"{1,2}({action}[^"]+?)"+,""",
  ]
 }
duo-app-activity-1 = {
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"event-name":"({event_name}[^"]+)"""",
    """"action":"({operation}[^"]+)"""",
    """"username":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[^"]+))"""",
    """"object":"({object}[^"]+)"""",
    """"src-application-name":"({app}[^"]+)"""",
  
}
```