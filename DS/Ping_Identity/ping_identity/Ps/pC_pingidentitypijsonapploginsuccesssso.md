#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-login-success-sso
  Conditions = [ """"EventType": "SSO"""", """"Status": "success"""" ]
  ParserVersion = "v1.0.0"

s-ping-events = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Fields = [
    """"Time":\s*"*({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+)""",
    """"duid":\s*"(({domain}[^"@\\\/]+)[\\\/]+)?({user}[^@"\\\/]+)"""",
    """"duid":\s*"({email_address}[^"\s@]+@[^"\s@]+)""""
    """"SRCIP":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"remoteAddr":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"Status":\s*"({result}[^"]+)""",
    """"Protocol":\s*"({protocol}[^"]+)""",
    """"PingHost":\s*"({host}[^"]+)""",
    """"EventType":\s*"({operation}[^"]+)""",
    """"DescriptionFail":\s*"({failure_reason}[^"]+)""",
  
}
```