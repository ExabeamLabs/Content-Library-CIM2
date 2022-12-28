#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-endpoint-login-userloginfail
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Conditions = [ """"event_simpleName":"UserLogonFailed""" ]
  Fields = [
    """"timestamp":\s*"*({time}\d{13})"""",
    """"UserName":\s*"({email_address}[^"@]+@[^"@]+)"""",
    """"UserName":\s*"(-|\/+|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[^"@\s]+))"""",
    """"UserSid":\s*"({user_sid}[^"]+)"""",
    """"event_simpleName":"({event_code}[^"]+)""",
    """"aid":"({aid}[^"]+)""",
    """"aip":\s*"({aip}[a-fA-F:\d.]+)"""",
    """"LogonType":"({login_type}\d+)"""",
    """"name":"({event_name}[^"]+)"""",
    """"LogonDomain":"({domain}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```