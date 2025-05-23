#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch_sec"
  Conditions = [
    """ADAuditPlus"""
    """EVENT_NUMBER = 4771"""
    """Kerberos pre-authentication failed"""
  ]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})"""
    """({host}[\w\-.]+) ADAuditPlus"""
    """USERNAME\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """CLIENT_IP_ADDRESS\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """CLIENT_HOST_NAME\s*=\s*({src_host}[\w\-.]+?)\s*\]"""
    """DOMAIN\s*=\s*([^\/]+\/)?({domain}[^\\\/]+?)\s*\]"""
    """SOURCE\s*=\s*({src_host}[\w\-.]+)"""
    """RECORD_NUMBER\s*=\s*({event_id}\d+)"""
    """EVENT_NUMBER\s*=\s*({event_code}\d+)"""
    """USER_SID\s*=\s*\%\{({user_sid}[^\}]+)"""
    """ERROR_CODE\s*=\s*({result_code}[^\s]+)"""
    """EVENT_TYPE_TEXT\s*=\s*({result}.+?)\s*\]"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```