#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-ds-object-modify-success-4742
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Conditions = [ """ADAuditPlus""", """EVENT_NUMBER = 4742""", """REMARKS = A computer account was changed.""" ]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})""",
    """({host}[\w\-.]+) ADAuditPlus""",
    """CLIENT_USER_NAME\s*=\s*(null|-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\]""",
    """CLIENT_USER_DOMAIN\s*=\s*(null|-|NT AUTHORITY|({domain}[^\s\]]+))\s*\]""",
    """CALLER_USER_NAME\s*=\s*(null|-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\]""",
    """CALLER_USER_DOMAIN\s*=\s*(null|-|NT AUTHORITY|({domain}[^\s\]]+))\s*\]""",
    """SOURCE\s*=\s*({src_host}[\w\-.]+)""",
    """RECORD_NUMBER\s*=\s*({event_id}\d+)""",
    """EVENT_NUMBER\s*=\s*({event_code}\d+)""",
    """CALLER_USER_SID\s*=\s*\%?\{?({user_sid}[^\s\}]+)""",
    """CALLER_LOGON_ID\s*=\s*(null|-|({login_id}[^\s]+))""",
    """ATTRIBUTES_TEXT\s*=\s*(-|null|({attribute}[^\s]+))""",
    """ACCOUNT_NAME\s*=\s*(null|-|({account_name}[^\s]+))""",
    """FORMAT_MESSAGE\s*=\s*(null|-|({object_type}[^\']+?))\s*'""",
    """REMARKS\s*=\s*(null|-|({operation_type}[^\]]+?))\s*\]""",
    """ATTRIBUTES_NEW_VALUE\s*=\s*(null|-|({new_attribute}[^\]]+?))\s*\]""",
    """ATTRIBUTES_OLD_VALUE\s*=\s*(null|-|({old_attribute}[^\]]+?))\s*\]""",
    """CLIENT_IP_ADDRESS\s*=\s*(null|-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]
  DupFields =[ "host->dest_host", "operation_type->event_name", "object_type->additional_info", "account_name->object" ]
  ParserVersion = "v1.0.0"


}
```