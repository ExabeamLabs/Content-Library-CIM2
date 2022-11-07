#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-login-fail-sso
  Conditions = [ """"EventType": "SSO"""", """"Status": "failure"""" ]
  ParserVersion = "v1.0.0"

s-ping-events = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Fields = [
    """"Time":\s*"*({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+)""",
    """"duid":\s*"(({domain}[^"@\\\/]+)[\\\/]+)?({user}[^@"\\\/]+)"""",
    """"duid":\s*"({email_address}[^"\s@]+@[^"\s@]+)""""
    """"SRCIP":\s*"({src_ip}[a-fA-F\d.:]+)""",
    """"remoteAddr":\s*"({dest_ip}[a-fA-F\d.:]+)""",
    """"Status":\s*"({result}[^"]+)""",
    """"Protocol":\s*"({protocol}[^"]+)""",
    """"PingHost":\s*"({host}[^"]+)""",
    """"EventType":\s*"({operation}[^"]+)""",
    """"DescriptionFail":\s*"({failure_reason}[^"]+)""",
  
}
```