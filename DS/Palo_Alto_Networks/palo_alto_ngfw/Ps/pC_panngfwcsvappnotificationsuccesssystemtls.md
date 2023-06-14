#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-notification-success-systemtls
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """,SYSTEM,tls,""", """,tls-edl-auth-failure,""" ]
  Fields = [
    """,SYSTEM,tls,[^,]*,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """,({asset_id}\d+),SYSTEM,""",
    """({event_category}SYSTEM)""",
    """,SYSTEM,({subtype}[^,]+),""",
    """,SYSTEM,([^,]*,){4}({event_code}[^,]+),""",
    """,SYSTEM,([^,]*,){5}\s*({object}[^,]+),""",
    """,SYSTEM,([^,]*,){9}({severity}[^,]+),""",
    """,SYSTEM,(?:[^,]*,){10}"*({event_name}[^"]+?)(?:\.*"|\.\s)""",
    """\d\d\s\d\d:\d\d:\d\d (-|({host}[\w\.\-]+))\s""",
    """,SYSTEM,(?:[^,]*,){10}"*({additional_info}[^"]+)"""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = "v1.0.0"


}
```