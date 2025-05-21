#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-endpoint-login-success-4648
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """明示的な資格情報を使用してログオンが試行されました。""" ]
  Fields = [ 
    """ComputerName =({computer_name}[\w.\-]+)""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4648),""",
    """EventCode=({event_code}\w+)""",
    """(?!\d+)({host}[\w\-.]+),([^,]*,)?明示的な資格情報を使用してログオンが試行されました。""",
    """サブジェクト:\s+セキュリティ ID:\s+({user_sid}[^\s]+)\s+アカウント名:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+>アカウント ドメイン:\s+({domain}[^\s]+)\s+ログオン ID:\s+({login_id}[^\s]+)\s+""",
    """資格情報が使用されたアカウント:\s+アカウント名:\s+({dest_user}[^\s]+)\s+アカウント ドメイン:\s+({dest_domain}[^\s]+)\s+"""
    """ターゲット サーバー名:\s+({dest_host}[^\s]+)""",
    """プロセス ID:\s+({process_id}\w+)\s+プロセス名:\s+({process_path}({process_dir}.*?\\)({process_name}[^\\]*?))\s+ネットワーク情報:""",
    """ネットワーク アドレス:\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]
  DupFields = [ "computer_name->host" ]


}
```