#### Parser Content
```Java
{
Name = microsoft-adfs-kv-app-authentication-fail-413
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Active Directory Federation Services
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ AD_FS_Auditing[""", """ AUDIT_FAILURE 413 """ ]
  Fields = [
    """({host}[\w\-.]+)\s+AD_FS_Auditing\[\d+\]:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """AUDIT_FAILURE\s+({event_code}\d+)\s+(({domain}[^\\\s]+)\\+)?({service_name}[^\\\s]+)\s+({failure_reason}[^\.]+?)\.""",
    """Caller:\s*(({domain}[^\\\s]+)\\+)?({user}[^\\\s]+)""",
    """Client IP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]


}
```