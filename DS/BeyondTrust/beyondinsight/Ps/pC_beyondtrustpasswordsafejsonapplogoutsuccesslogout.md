#### Parser Content
```Java
{
Name = beyondtrust-passwordsafe-json-app-logout-success-logout
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","MMM dd yyyy hh:mm:ss a"]
  Conditions = [ """"vendor":"BeyondTrust"""", """"category":"Logout"""", """"product":"BeyondInsight"""", """"systemname":"Logout"""" ]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"createdate":"({time}\w+\s+\d\d\s+\d\d\d\d\s+\d\d:\d\d:\d\d\s+\w+)"""",
    """"username":"(({domain}[^\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"(sourceip|ipaddress)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"sourcehost":"({src_host}[^"]+)"""",
    """"({app}BeyondInsight)"""",
    """"category":"({event_name}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```