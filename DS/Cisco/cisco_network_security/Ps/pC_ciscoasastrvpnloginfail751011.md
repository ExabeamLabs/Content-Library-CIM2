#### Parser Content
```Java
{
Name = "cisco-asa-str-vpn-login-fail-751011"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""-751011"""
"""%ASA-"""
]
Fields = [
"""({host}[\w\-.]+)\s+({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)"""
""":\s*Local\s*:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)\s"""
"""\sRemote\s*:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)\s"""
"""({event_name}Failed user authentication)"""
"""Username\s*:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\sError\s*:\s*({failure_reason}.+?)\s*$"""
]
ParserVersion = "v1.0.0"


}
```