#### Parser Content
```Java
{
Name = beyondtrust-passwordsafe-json-app-login-fail-loginfailure
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """"vendor":"BeyondTrust"""", """"eventname":"Login"""", """"category":"Login Failure"""", """"product":"BeyondInsight"""", """"message":"""", """"systemname":"Login Failure"""" ]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"createdate":"({time}\d{1,2}\/\d{1,2}\/\d\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2}\s\w{1,2})"""",
    """"username":"(({domain}[^\"]+)\\+)?({user}[^"]+)"""",
    """"(sourceip|ipaddress)":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"sourcehost":"({src_host}[^"]+)"""",
    """"({app}BeyondInsight)"""",
    """"category":"({event_name}[^"]+)"""",
    """"eventname":"({additional_info}[^"]+)"""",
    """"message":"({failure_reason}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```