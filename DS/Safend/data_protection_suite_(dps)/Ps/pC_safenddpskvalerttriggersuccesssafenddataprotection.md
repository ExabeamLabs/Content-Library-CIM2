#### Parser Content
```Java
{
Name = safend-dps-kv-alert-trigger-success-safenddataprotection
  ParserVersion = v1.0.0
  Vendor = Safend
  Product = Data Protection Suite (DPS)
  TimeFormat = "M d yyyy HH:mm:ss"
  Conditions = [ """[Safend Data Protection]""", """ Client Alert details:""" ]
  Fields = [
    """Client GMT:\s+({time}\d+/\d+/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))""",
    """Action:\s*({result}[^,]+)""",
    """User:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({email_domain}[^@,.\s]+))?""",
    """User:\s*({email_address}[^\s,]+)""",
    """Computer:\s*({host}[^,]+)""",
    """Operating System:\s*({os}[^,]+)""",
    """Policy:\s*({alert_name}[^,]+)""",
    """Policy:\s*.+?\-\s*({alert_type}[^,\-]+?)\s*\-""",
    """Scope:\s*({alert_type}[^,]+),""",
    """({additional_info}Device Info:\s*\S[^:]+?),\s+[^,:]+?:""",
    """Device Type:\s*(?:N/A|({protocol}[^,]+))""",
    """Distinct ID:\s*(|({device_id}[^,]+)),""",
    """Details:\s*Disk size = (?i)({bytes}\d+\s+\w+)""",
    """Details:\s*({process_name}[^=:,]+?)(,|\s*$)"""
  ]


}
```