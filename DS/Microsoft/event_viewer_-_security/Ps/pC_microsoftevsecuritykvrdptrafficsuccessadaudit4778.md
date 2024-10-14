#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-rdp-traffic-success-adaudit-4778"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch_sec"
  Conditions = [
    """4778"""
    """[ REMARKS = A session was reconnected to a Window Station"""
    """[ SOURCE = """
    """[ USERNAME ="""
  ]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})"""
    """({host}[\w\-.]+) ADACategory"""
    """({host}[\w\-.]+) ADAuditPlus"""
    """USERNAME\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """DOMAIN\s*=\s*({domain}[^\s\]]+)"""
    """CLIENT_HOST_NAME\s*=\s*({dest_host}[\w\-.]+?)\s*\]"""
    """SOURCE\s*=\s*({src_host}[\w\-.]+)"""
    """RECORD_NUMBER\s*=\s*({event_id}\d+)"""
    """({event_code}4778)"""
    """USER_SID\s*=\s*(null|({user_sid}[^\s]+))"""
    """LOGON_ID\s*=\s*({login_id}[^\s]+)"""
    """REMARKS\s*=\s*({event_name}[^.\]]+)(\.)?\s+\]"""
    """CLIENT_IP_ADDRESS\s*=\s*(null|-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]


}
```