#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-4688-1
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """4688""", """新しいプロセスが作成されました。""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM|am|pm))"""
    """Computer(Name)?=({host}[\w.\-]+)""",
    """({event_code}4688)""",
    """({event_name}新しいプロセスが作成されました)。.+?セキュリティ ID:\s*({user_sid}.*?)\s*アカウント名:\s*({user}[\w\.\-]{1,40}\$?)\s*>アカウント ドメイン:\s*({domain}.*?)\s*ログオン ID:\s*({login_id}.*?)\s*ターゲット サブジェクト:""",
    """新しいプロセス ID:\s*({process_guid}.+?)\s*新しいプロセス名:""",
    """作成元プロセス ID:\s*({parent_process_guid}.+?)\s*作成元プロセス名:"""
    """新しいプロセス名:\s*({process_path}({process_dir}.+?[\\\/])?({process_name}[^\\\/"]+?))\s*トークン昇格の種類:""",
    """プロセスのコマンド ライン:\s*(\s+|({process_command_line}[^=]+))\s+トークン昇格の種類は"""
  ]


}
```