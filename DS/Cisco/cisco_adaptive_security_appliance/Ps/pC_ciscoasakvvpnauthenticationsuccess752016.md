#### Parser Content
```Java
{
Name = cisco-asa-kv-vpn-authentication-success-752016
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  Conditions = [ """%FTD-5-752016:""" ]

cisco-events-1 = {
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """Session=({session_id}\S+),""",
    """User(=|\s)<?({user}[^,>]+)""",
    """\sGroup\s*<({group_name}[^>]+)>"""
  
}
```