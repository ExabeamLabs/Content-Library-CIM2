#### Parser Content
```Java
{
Name = "cisco-duo-str-app-authentication-success-loginfor"
Vendor = "Cisco"
Product = "Duo Access"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""") Successful Duo login for """
]
Fields = [
"""\) Successful Duo login for \'(({domain}[^\\]+)\\)?({user}[^']+)"""
"""\d\d:\d\d \(({session_id}\d+)\)"""
]
ParserVersion = "v1.0.0"


}
```