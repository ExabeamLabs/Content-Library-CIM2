#### Parser Content
```Java
{
Name = beyondtrust-passwordsafe-json-app-login-fail-loginfailure
  Vendor = BeyondTrust
  Product = BeyondTrust PasswordSafe
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """"vendor":"BeyondTrust"""", """"eventname":"Login"""", """"category":"Login Failure"""", """"product":"BeyondInsight"""", """"message":"""", """"systemname":"Login Failure"""" ]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"createdate":"({time}\d{1,2}\/\d{1,2}\/\d\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2}\s\w{1,2})"""",
    """"username":"(({domain}[^\"]+)\\+)?({user}[^"]+)"""",
    """"(sourceip|ipaddress)":"({src_ip}[a-fA-F\d:.]+)"""",
    """"sourcehost":"({src_host}[^"]+)"""",
    """"({app}BeyondInsight)"""",
    """"category":"({event_name}[^"]+)"""",
    """"eventname":"({additional_info}[^"]+)"""",
    """"message":"({failure_reason}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```