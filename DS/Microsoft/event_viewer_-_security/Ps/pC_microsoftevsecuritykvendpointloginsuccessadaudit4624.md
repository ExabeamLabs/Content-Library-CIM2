#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-adaudit-4624"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch_sec"
  Conditions = [
    """ADAuditPlus"""
    """EVENT_NUMBER = 4624"""
    """An account was successfully logged on"""
  ]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})"""
    """({host}[\w\-.]+) ADAuditPlus"""
    """CALLER_USER_NAME\s*=\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """CLIENT_IP_ADDRESS\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """CLIENT_HOST_NAME\s*=\s*({src_host}[\w\-.]+)"""
    """CALLER_USER_DOMAIN\s*=\s*(null|-|({domain}[^\\\/\s]+))"""
    """SOURCE\s*=\s*(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({dest_host}[\w\-.]+))"""
    """RECORD_NUMBER\s*=\s*({event_id}\d+)"""
    """EVENT_NUMBER\s*=\s*({event_code}\d+)"""
    """USER_SID\s*=\s*\%\{({user_sid}[^\}]+)"""
    """LOGON_ID\s*=\s*(null|-|({login_id}[^\s]+))"""
    """LOGON_TYPE\s*=\s*({login_type}\d+)"""
    """LOGON_PROCESS\s*=\s*(null|-|({auth_process}[^\s]+))"""
    """AUTHENTICATION_PACKAGE\s*=\s*(null|-|({auth_package}[^\s]+))"""
    """CALLER_PROCESS_NAME\s*=\s*(?:-|null|({process_path}[\w:\\.\-]+?\\+({process_name}[^\\\]]+)))\s+\]"""
    """USER_SAM_ACCOUNT_NAME\s*=\s*(-|null|({account}[^\s\]]+))"""
    """REMARKS\s*=\s*({event_name}[^\]]+?)\s*\]"""
    """KEY_LENGTH\s*=\s*({key_length}\d+)\s+\]"""
  ]


}
```