#### Parser Content
```Java
{
Name = "cisco-duo-str-app-authentication-success-ipaddress"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""") IP address: """
]
Fields = [
"""\) IP address: ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\d\d:\d\d \(({session_id}\d+)\)"""
]
ParserVersion = "v1.0.0"


}
```