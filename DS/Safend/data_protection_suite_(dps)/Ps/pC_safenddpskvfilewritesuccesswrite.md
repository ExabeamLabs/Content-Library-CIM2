#### Parser Content
```Java
{
Name = safend-dps-kv-file-write-success-write
  ParserVersion = v1.0.0
  Vendor = Safend
  Product = Data Protection Suite (DPS)
  TimeFormat = "MM dd yyyy HH:mm:ss"
  Conditions = [ """[Safend Data Protection]""", """Action: Write""" ]
  Fields = [
    """Client GMT:\s+({time}\d+/\d+/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))""",
    """Action:\s*({operation}[^,]+?)\s*$""",
    """User:\s*({user}[\w\.\-]{1,40}\$?)(@({email_domain}[^@,.\s]+))?""",
    """User:\s*({email_address}[^,\s]+)""",
    """Computer:\s*({host}[^,]+)""",
    """Operating System:\s*({os}[^,]+)""",
    """Device Type:\s*({device_type}[^,]+)""",
    """Device Info:\s*({device_type}[^,]+),""",
    """Distinct ID:\s*(|({device_id}[^,]+)),""",
    """({operation_details}Policy:\s*[^,]+)""",
    """File Name:\s*({src_file_path}[^,]+)""",
    """File Name:\s*.+?\\({src_file_name}[^\\,]+),""",
    """File Name:[^,]+\.({src_file_ext}\w+),""",
    """File Type:\s*({src_file_ext}\w+)""",
    """File Size:\s*({bytes}\d+)"""
  ]


}
```