#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-activity-general
  ParserVersion = v1.0.0
  Product = Palo Alto NGFW
  Conditions = [ """,SYSTEM,""", """,SYSTEM,general,""" ]
  Fields=${DLPaloAltoParsersTemplates.pan-system-1.Fields}[
    """SYSTEM,({event_subtype}[^,]+),([^,]*,){3}([^,]+),""", #dl field removed
# job_id is removed
    """User:\s*({user}[^\s"\.]+)""",
# commit_description is removed
    """({event_name}Failed password for root)\s+\w+\s+({src_ip}[a-fA-F\d:.]+)\s+port\s+({src_port}\d+)\s+({user}[^"]+)"""
  ]

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
    """User\s*(name:)?\s+({email_address}[^@\s]+@[^\s,]+?)(\.\\"|\.")?,""",
    """Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
    ]
  DupFields = ["host->dest_host"
}
```