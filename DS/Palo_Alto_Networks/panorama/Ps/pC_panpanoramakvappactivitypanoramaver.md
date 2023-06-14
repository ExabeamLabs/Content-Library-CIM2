#### Parser Content
```Java
{
Name = pan-panorama-kv-app-activity-panoramaver
  Vendor = Palo Alto Networks
  Product = Panorama
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """,SYSTEM,""", """ PAN-OS """, """Panorama ver""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),""",
    """Client IP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Server IP:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """,SYSTEM,({protocol}[^,]+),""",
    """,SYSTEM,([^,]*,){4}({operation}[^,]+),""",
    """,({dest_host}[\w\-.]+)\s*$""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    
  ]


}
```