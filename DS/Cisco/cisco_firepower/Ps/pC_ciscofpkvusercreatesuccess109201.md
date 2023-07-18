#### Parser Content
```Java
{
Name = cisco-fp-kv-user-create-success-109201
  ParserVersion = "v1.0.0"
  Conditions = [ """%FTD-5-109201: """, """UAUTH:""" ]

cisco-events-1 = {
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """Session=({session_id}\S+),""",
    """User(=|\s)<?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\-\.]{1,40}))([\>,]+)?\s""",
    """\sGroup\s*<({group_name}[^>]+)>"""
  
}
```