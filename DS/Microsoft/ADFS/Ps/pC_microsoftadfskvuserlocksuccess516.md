#### Parser Content
```Java
{
Name = microsoft-adfs-kv-user-lock-success-516
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = ADFS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ AD_FS_Auditing[""", """ AUDIT_FAILURE 516 """ ]
  Fields = [
    """({host}[\w\-.]+)\s+AD_FS_Auditing\[\d+\]:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """AUDIT_FAILURE\s+({event_code}\d+)\s+(({domain}[^\\\s]+)\\+)?({service_name}[^\\\s]+)\s+({failure_reason}[^\.]+?)\.""",
    """Client IP:\s*({src_ip}[A-Fa-f:\d.]+)""",
    """User:\s*({email_address}[^\s@]+@[^\s@]+)""",
  ]


}
```