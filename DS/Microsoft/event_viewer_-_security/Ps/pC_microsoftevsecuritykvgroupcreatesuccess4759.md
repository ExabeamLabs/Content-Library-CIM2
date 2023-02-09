#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-create-success-4759
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  Conditions = [ """ [ EVENT_NUMBER = 4759 ] """, """ ADAuditPlus: """, """ [ SOURCE = """, """ [ FORMAT_MESSAGE = """ ]
  Fields = ${MicrosoftParserTemplates.ad-audit-plus.Fields}[
    """Category\s*=\s*({category}[^\s]+)"""
]

ad-audit-plus = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})""",
    """({host}[\w\-.]+) ADAuditPlus""",
    """CLIENT_USER_NAME\s*=\s*(null|-|SYSTEM|({user}[^\s\]]+))\s*\]""",
    """CLIENT_USER_DOMAIN\s*=\s*(null|-|NT AUTHORITY|({domain}[^\s\]]+))\s*\]""",
    """CALLER_USER_NAME\s*=\s*(null|-|SYSTEM|({user}[^\s\]]+))\s*\]""",
    """CALLER_USER_DOMAIN\s*=\s*(null|-|NT AUTHORITY|({domain}[^\s\]]+))\s*\]""",
    """SOURCE\s*=\s*({src_host}[\w\-.]+)""",
    """RECORD_NUMBER\s*=\s*({event_id}\d+)""",
    """EVENT_NUMBER\s*=\s*({event_code}\d+)""",
    """CALLER_USER_SID\s*=\s*\%?\{?({user_sid}[^\s\}]+)""",
    """CALLER_LOGON_ID\s*=\s*(null|-|({login_id}[^\s]+))""",
    """ATTRIBUTES_TEXT\s*=\s*(-|null|({attribute}[^\s]+))""",
    """ACCOUNT_NAME\s*=\s*(null|-|({object}[^\s]+))""",
    """REMARKS\s*=\s*(null|-|({event_name}[^.\]]+))(\.)?\s+\]""",
    """FORMAT_MESSAGE\s*=\s*(null|-|({additional_info}[^.\]]+))(\.)?\s+\]""",
    """ATTRIBUTES_NEW_VALUE\s*=\s*(null|-|({new_attribute}[^\]]+))\s*\]""",
    """ATTRIBUTES_OLD_VALUE\s*=\s*(null|-|({old_attribute}[^\]]+))\s*\]""",
 ]
  DupFields = [ "host->dest_host" 
}
```