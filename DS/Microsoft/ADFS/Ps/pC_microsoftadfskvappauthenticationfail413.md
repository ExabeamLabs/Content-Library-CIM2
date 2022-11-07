#### Parser Content
```Java
{
Name = microsoft-adfs-kv-app-authentication-fail-413
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = ADFS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ AD_FS_Auditing[""", """ AUDIT_FAILURE 413 """ ]
  Fields = [
    """({host}[\w\-.]+)\s+AD_FS_Auditing\[\d+\]:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """AUDIT_FAILURE\s+({event_code}\d+)\s+(({domain}[^\\\s]+)\\+)?({service_name}[^\\\s]+)\s+({failure_reason}[^\.]+?)\.""",
    """Caller:\s*(({domain}[^\\\s]+)\\+)?({user}[^\\\s]+)""",
    """Client IP:\s*({src_ip}[A-Fa-f:\d.]+)""",
  ]


}
```