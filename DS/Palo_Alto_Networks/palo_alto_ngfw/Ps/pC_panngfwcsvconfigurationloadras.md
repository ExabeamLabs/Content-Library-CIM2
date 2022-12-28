#### Parser Content
```Java
{
Name = pan-ngfw-csv-configuration-load-ras
  ParserVersion = v1.0.0
  Product = Palo Alto NGFW
  Conditions = [ """,SYSTEM,""", """,SYSTEM,ras,""" ]

pan-system-1 {
  Vendor = Palo Alto Networks
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Fields = [
    """SYSTEM,([^,]+,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),""",
    """SYSTEM[^"]+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """SYSTEM,("[^"]*",|[^,]*,){18}({host}[\w\-\.]+)""",
    """:\d\d:\d\d\s+({host}[\w.-]+)\s""",
    """,({host_id}\d+),SYSTEM,""",
    """({event_category}SYSTEM)""",
    """SYSTEM,({event_subtype}[^,]+),""",
    """SYSTEM,([^,]*,){9}({severity}[^,]+),""",
    """SYSTEM,(?:[^,]*,){10}"*({additional_info}[^",]+?)(?:\.*"|\.\s|\.*,|\s(\d{1,3}\.){3}\d{1,3}:\d+)""",
    """Private IP:\s?({src_translated_ip}[^,\s]+)""",
    """User\s*(name:)?\s+({user}[\w.'\-\\$]+?)\.?(\s|,|"|$)""",
    """User\s*(name:)?\s+({email_address}[^@\s]+@[^\s,]+),""",
    """Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
    ]
  DupFields = ["host->dest_host"
}
```