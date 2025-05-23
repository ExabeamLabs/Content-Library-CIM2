#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-authentication-success-adaudit-4768"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch_sec"
  Conditions = [
    """ADAuditPlus"""
    """EVENT_NUMBER = 4768"""
  ]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})"""
    """({host}[\w\-.]+) ADAuditPlus"""
    """USERNAME\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\]"""
    """USERNAME\s*=\s*({user_upn}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)\s*\]"""
    """New Logon:[^"]*?Account Name(:|=)\s*(-|SYSTEM|(({user_upn}[^\s\]@]+@[^\s\]@]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """CLIENT_IP_ADDRESS\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """DOMAIN\s*=\s*({domain}[^\\\/\]]+?)\s*\]"""
    """RECORD_NUMBER\s*=\s*({event_id}\d+)"""
    """EVENT_NUMBER\s*=\s*({event_code}\d+)"""
    """USER_SID\s*=\s*\%?\{?({user_sid}[^\}\s\]]+)"""
    """ERROR_CODE\s*=\s*({result_code}[^\s]+)"""
    """EVENT_TYPE_TEXT\s*=\s*({result}.+?)\s*\]"""
    """LOGON_SERVICE\s*=\s*(null|-|({service_name}[^\s\]]+))"""
    """TICKET_OPTIONS\s*=\s*(null|-|({ticket_options}[^\s\]]+))"""
    """TICKET_ENCRYPTION_TYPE\s*=\s*(null|-|({ticket_encryption_type}[^\s\]]+))"""
  ]


}
```