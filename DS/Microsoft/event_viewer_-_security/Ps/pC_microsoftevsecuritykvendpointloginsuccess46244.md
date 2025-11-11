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
    """ComputerName =({dest_host}({host}[\w.\-]+))""",
    """(?!\d+)({dest_host}({host}[\w\-.]+)),([^,]*,)?アカウントが正常にログオンしました。""",
    """({event_code}4624)""",
    """ログオン タイプ:\s+({login_type}\d+)""",
    """新しいログオン:.*?アカウント名:\s+(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+アカウント ドメイン:\s+(?:-|({domain}[^\\\s]+?))\s*ログオン ID:""",
    """プロセス名:\s+(-|({process_path}[\w:\\.\-]+))""",
    """ソース ネットワーク アドレス:\s+(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """ログオン プロセス:\s+({auth_process}[^\s]+)\s+認証パッケージ:\s+({auth_package}[^\s]+)""",
    """ログオン ID:\s+({login_id}[^\s]+)""",
    """新しいログオン:\s+セキュリティ ID:\s+({user_sid}[^\s]+)\s"""
    """移行されたサービス:\s+-\s+パッケージ名\s+\(NTLM\s+のみ\):\s+({auth_package}.+?)\s+キーの長さ"""
  ]


}
```