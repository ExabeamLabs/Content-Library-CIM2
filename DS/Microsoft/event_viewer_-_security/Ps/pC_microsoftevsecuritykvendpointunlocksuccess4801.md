#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-unlock-success-4801"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch_sec"
  Conditions = [
    """ADAuditPlus"""
    """EVENT_NUMBER = 4801"""
    """REMARKS = The workstation was unlocked."""
  ]
  Fields = [
    """({host}[\w\-.]+)\s+ADAuditPlus"""
    """\WTIME_GENERATED\s*=\s*({time}\d{10})"""
    """\WREMARKS\s*=\s*({event_name}[^\]]+?)\s*\]"""
    """\WEVENT_NUMBER\s*=\s*({event_code}\d+)"""
    """\WEVENT_TYPE_TEXT\s*=\s*(null|-|({result}[^\]]+?))\s*\]"""
    """\WSOURCE\s*=\s*(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[\w\-.]+))"""
    """\WLOGON_ID\s*=\s*(null|-|({login_id}[^\]]+?))\s*\]"""
    """\WDOMAIN\s*=\s*(null|-|({domain}[^\s\]]+?))\s*\]"""
    """\WCALLER_PROCESS_NAME\s*=\s*(|null|-|({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/\"\]]+?)))\s*\]"""
    """\WCLIENT_HOST_NAME\s*=\s*(null|({dest_host}[\w\-.]+))"""
    """\WCLIENT_IP_ADDRESS\s*=\s*(null|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
    """\WUSERNAME\s*=\s*(null|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\]"""
    """\WRECORD_NUMBER\s*=\s*(null|({event_id}\d+))"""
    """\WUSER_SID\s*=\s*\%?\{?(null|-|({user_sid}[^\s\]\}]+))"""
    """\WFORMAT_MESSAGE\s*=\s*(null|-|({additional_info}.+?))\s*\]"""
    """\WERROR_CODE\s*=\s*(null|-|({result_code}[^\s\]]+))"""
    """\WLOGON_TYPE\s*=\s*({login_type}\d+)"""
    """\WLOGON_PROCESS\s*=\s*(null|-|({auth_process}[^\s]+))"""
    """\WAUTHENTICATION_PACKAGE\s*=\s*(null|-|({auth_package}[^\s]+))"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```