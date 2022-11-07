#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-4624-4
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """4624""", """アカウントが正常にログオンしました。""" ]
  Fields = [ 
    """({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),4624,""",
    """ComputerName =({host}[\w.\-]+)""",
    """(?!\d+)({host}[\w\-.]+),([^,]*,)?アカウントが正常にログオンしました。""",
    """({event_code}4624)""",
    """ログオン タイプ:\s+({login_type}\d+)""",
    """新しいログオン:.*?アカウント名:\s+(?:-|({user}[^\\\s]+?))\s+アカウント ドメイン:\s+(?:-|({domain}[^\\\s]+?))\s*ログオン ID:""",
    """プロセス名:\s+(-|({process_path}[\w:\\.\-]+))""",
    """ソース ネットワーク アドレス:\s+(::1|({src_ip}[\w:.]+))""",
    """ログオン プロセス:\s+({auth_process}[^\s]+)\s+認証パッケージ:\s+({auth_package}[^\s]+)""",
    """ログオン ID:\s+({login_id}[^\s]+)""",
    """新しいログオン:\s+セキュリティ ID:\s+({user_sid}[^\s]+)\s"""
  ]
  DupFields = [ "host->dest_host" ]


}
```