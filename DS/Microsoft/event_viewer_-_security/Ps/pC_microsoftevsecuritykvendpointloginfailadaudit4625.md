#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4625"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch_sec"
  Conditions = [
    """ADAuditPlus"""
    """EVENT_NUMBER = 4625"""
  ]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})"""
    """({host}[\w\-.]+) ADAuditPlus"""
    """\s(USERNAME|USER)\s*=\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
    """CLIENT_IP_ADDRESS\s*=\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """CLIENT_HOST_NAME\s*=\s*({dest_host}[\w\-.]+)"""
    """DOMAIN\s*=\s*({domain}[^\\\/\s]+)"""
    """SOURCE\s*=\s*({src_host_windows}[\w\-.]+)"""
    """RECORD_NUMBER\s*=\s*({event_id}\d+)"""
    """EVENT_NUMBER\s*=\s*({event_code}\d+)"""
    """USER_SID\s*=\s*({user_sid}[^\s]+)"""
    """LOGON_ID\s*=\s*(null|({login_id}[^\s]+))"""
    """LOGON_TYPE\s*=\s*({login_type}\d+)"""
    """LOGON_PROCESS\s*=\s*(null|({auth_process}[^\s]+))"""
    """AUTHENTICATION_PACKAGE\s*=\s*({auth_package}[^\s]+)"""
    """CALLER_PROCESS_NAME\s*=\s*(|null|-|({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?)))\s*\]"""
    """CALLER_USER_NAME\s*=\s*(-|({src_user}[^\s]+))"""
    """CALLER_USER_DOMAIN\s*=\s*(-|({src_domain}[^\s]+))"""
    """FAILURE_STATUS\s*=\s*({result_code}[^\s]+)"""
    """FAILURE_SUB_STATUS\s*=\s*({result_code}[^\s]+)"""
  ]


}
```