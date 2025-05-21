#### Parser Content
```Java
{
Name = cisco-fp-kv-alert-trigger-success-722035
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-3-722035""", """ Received large packet """ ]
  Fields = [
    """({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-.]+)\s:\s*%FTD-"""
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d)-({event_code}[^:]+)"""
    """Group\s+<?({group_name}[^>\s]+)>?"""
    """User\s+<?({user}[\w\.\-\!\#\^\~]{1,40}\$?)>?"""
    """IP\s+<?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>?"""
    """({event_name}Received large packet)\s+({bytes}\d+)"""
]


}
```