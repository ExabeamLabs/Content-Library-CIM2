#### Parser Content
```Java
{
Name = "cisco-asa-kv-endpoint-login-fail-113015"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Conditions = [
"""-113015"""
""": AAA user authentication Rejected"""
]
Fields = [
"""({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%\w+\-""",
"""({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)\s*(({host}[\w.\-]+))?.*?%\w+-({priority}\d+)-({event_code}\d+)"""
"""({event_name}AAA user authentication Rejected)"""
"""\sreason\s*=\s*({failure_reason}.+?)\s*:"""
"""\suser\s*=\s*((\*+?)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*:"""
"""\suser IP\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```