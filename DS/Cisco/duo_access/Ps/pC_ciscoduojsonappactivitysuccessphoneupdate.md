#### Parser Content
```Java
{
Name = cisco-duo-json-app-activity-success-phoneupdate
  Product = Duo Access
  Conditions = [ """action=phone_update;""", """object=""", """timestamp=""" ]
  ParserVersion = "v1.0.0"

q-duo-app-activity = {
  Vendor = Cisco
  TimeFormat = ["MM/dd/yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Fields = [
    """"ts"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)"""
    """\d\d:\d\d\s+({host}.+?)\s+(\S+\s+)*@\{action=({operation}[^;]+)""",
    """username=(?![^:]+:\s*[^;\}]+)({full_name}[^;\}]+)""",
    """"uname"+:\s*"{1,2}({user}[\w\.\-]{1,40}\$?)"+,""",
    """"realname"+:\s*"{1,2}({full_name}[^"]+?)"+,""",
    """object=\s*({object}[^;]+?)(?:;|\})""",
    """timestamp=\s*({time}\d+\/\d+\/\d\d\d\d \d+:\d\d:\d\d)""",
    """"email"+:\s*"{1,2}({email_address}[^@]+@({email_domain}[^"]+?))"+,""",
    """"ip_address"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"primary_auth_method"+:\s*"{1,2}({auth_method}[^"]+?)"+,""",
    """"factor"+:\s*"{1,2}({factor}[^"]+?)"+,""",
  ]
 }
duo-app-activity-1 = {
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","epoch_sec"]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """destinationServiceName =({app}\S+)"""
    """"timestamp"\s*:\s*({time}\d{10})""",
    """"event-name":"({event_name}[^"]+)"""",
    """"action":"({operation}[^"]+)"""",
    """"description":\s*"\{({additional_info}[^"]+?)\}",""",
    """"username":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[\w\.\-]{1,40}\$?))"""",
    """"object":"({object}[^"]+)"""",
    """"error":\s*"({failure_reason}[^"]+)""",
    """"email\\"+:\s*\\"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\"""",
    """"ip_address"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"src-application-name":"({app}[^"]+)""""
  
}
```