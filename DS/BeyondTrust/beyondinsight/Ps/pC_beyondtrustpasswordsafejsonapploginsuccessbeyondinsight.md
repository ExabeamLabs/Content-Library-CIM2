#### Parser Content
```Java
{
Name = beyondtrust-passwordsafe-json-app-login-success-beyondinsight
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy HH:mm:ss a"]
  Conditions = [ """"vendor":"BeyondTrust"""", """"eventname":"Login"""", """"category":"PMM Login"""", """"product":"BeyondInsight"""", """"systemname":"PMM Login"""" ]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"createdate":"({time}\d{1,2}\/\d{1,2}\/\d\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2}\s\w{1,2})"""",
    """"username":"(({domain}[^\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"(sourceip|ipaddress)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"sourcehost":"({src_host}[^"]+)"""",
    """"({app}BeyondInsight)"""",
    """"category":"({event_name}[^"]+)"""",
    """"eventname":"({additional_info}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```