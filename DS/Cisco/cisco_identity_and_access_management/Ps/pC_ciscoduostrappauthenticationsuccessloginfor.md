#### Parser Content
```Java
{
Name = "cisco-duo-str-app-authentication-success-loginfor"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""") Successful Duo login for """
]
Fields = [
"""\) Successful Duo login for \'(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\d\d:\d\d \(({session_id}\d+)\)"""
]
ParserVersion = "v1.0.0"


}
```