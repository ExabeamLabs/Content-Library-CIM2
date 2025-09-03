#### Parser Content
```Java
{
Name = "cisco-asa-kv-vpn-login-fail-113005"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy MMM dd HH:mm:ss", "MMM dd yyyy HH:mm:ss"]
Conditions = [
"""-113005:"""
"""AAA user authentication Rejected :"""
""": user ="""
""": reason ="""
]
Fields = [
"""({time}(\w+\s)?\d+\s+(\w+\s+)?\d+\s+\d+:\d+:\d+)\s+(UTC\s+)?({host}[^\s]+)\s+:\s+%\w+\-"""
"""({event_code}130005)\s*:\s*({event_name}[^:]+?)\s*:\s\w+"""
"""({time}\d+\s+\w+\s+\d+\s+\d+:\d+:\d+)\s+UTC\s+({host}[^\s]+)\s+:\s+({event_code}[^\s]+):\s+({event_name}.+?)\s+:"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s*(({host}[\w.\-]+))?.*?({event_code}[^\s]+):\s+({event_name}.+?)\s+:"""
"""reason\s+=\s+({failure_reason}.+?)\s+:"""
"""server\s+=\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+:"""
""": user\s*=?\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""user IP\s+=\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```