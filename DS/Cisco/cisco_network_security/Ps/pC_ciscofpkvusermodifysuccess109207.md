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
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """Session=({session_id}\S+),""",
    """User(=|\s)<?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))([\>,]+)?\s""",
    """\sGroup\s*<({group_name}[^>]+)>"""
    """Local:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))(:({src_port}\d+))?"""
    """Remote:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))(:({dest_port}\d+))?"""
  
}
```