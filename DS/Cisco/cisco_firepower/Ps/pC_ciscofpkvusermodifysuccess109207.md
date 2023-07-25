#### Parser Content
```Java
{
Name = cisco-fp-kv-user-modify-success-109207
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """%FTD-5-109207: """ ]
  Fields = ${DLLMSCiscoParsersTemplates.cisco-events-1.Fields} [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
  ]

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