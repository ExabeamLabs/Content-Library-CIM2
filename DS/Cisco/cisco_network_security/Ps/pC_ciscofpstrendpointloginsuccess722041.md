#### Parser Content
```Java
{
Name = "cisco-fp-str-endpoint-login-success-722041"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""-722041"""
"""%FTD-"""
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)"""
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
"""%FTD-({priority}\d+)-({event_code}\d+)"""
"""User\s*<({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^>]+))?>"""
"""\sIP\s+<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>"""
"""Group\s+<({group_name}.+?)>"""
]
ParserVersion = "v1.0.0"


}
```