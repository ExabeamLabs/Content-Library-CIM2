#### Parser Content
```Java
{
Name = cisco-fp-str-ip-assign-737026
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """-737026""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """\sSession=({session_id}[^,]+)\s*""",
    """({event_name}Client assigned)""",
    """Client assigned (({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))"""
  ]


}
```