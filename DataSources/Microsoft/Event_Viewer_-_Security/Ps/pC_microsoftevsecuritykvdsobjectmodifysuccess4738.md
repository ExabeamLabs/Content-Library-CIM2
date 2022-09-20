#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-ds-object-modify-success-4738
  ParserVersion = "v1.0.0"
  Conditions = [ """ADAuditPlus""", """EVENT_NUMBER = 4738""", """REMARKS = A user account was changed.""" ]

ad-audit-ds-access = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d+)""",
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
    """FORMAT_MESSAGE\s*=\s*(null|-|({ds_object_class}[^\']+?))\s*'""",
    """REMARKS\s*=\s*(null|-|({operation_type}[^\]]+?))\s*\]""",
    """ATTRIBUTES_NEW_VALUE\s*=\s*(null|-|({new_attribute}[^\]]+?))\s*\]""",
    """ATTRIBUTES_OLD_VALUE\s*=\s*(null|-|({old_attribute}[^\]]+?))\s*\]""",
    """CLIENT_IP_ADDRESS\s*=\s*(null|-|({src_ip}[a-fA-F:\d.]+))"""
  ]
  DupFields =[ "host->dest_host", "operation_type->event_name", "ds_object_class->additional_info" 
}
```