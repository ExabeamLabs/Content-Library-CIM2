#### Parser Content
```Java
{
Name = "cisco-ios-str-configuration-modify-success-configured"
  Vendor = "Cisco"
  Product = "Cisco IOS"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """%SYS-"""
    """Configured from console"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d (?:-|({host}[^:\s]+)) \d+: """
    """({event_code}%SYS-[^\s]+):"""
    """({event_category}CONFIG)"""
    """%SYS-[^\s]+: ({event_name}.+?)\s*$"""
    """Configured from console by (({email_address}[^@\s]+@[^\.\s]+\.[^\s]+)|(({domain}[^\s\\]+)\\+)?({user}[^\s]+)) on""",
    """ on .+?\((({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^)]+))\)"""
  ]
  ParserVersion = "v1.0.0"


}
```