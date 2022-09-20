#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-file-read-success-4663-5
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """,4663,""", """オブジェクトへのアクセスが試行されました。""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4663),({host}[\w\-.]+)""",
    """サブジェクト:\s*\S+\s*ID:\s*({user_sid}\S+)""",
    """アカウント名:\s*({user}[^\s]+)""",
    """アカウント ドメイン:\s*({domain}[^\s]+)""",
    """ログオン ID:\s*({login_id}[^\s]+)""",
    """オブジェクトの種類:\s*({file_type}[^\s]+)""",
    """オブジェクト名:\s*({file_path}.+?)\s*ハンドル ID:""",
    """オブジェクト名:\s*({file_dir}.+?)({file_name}([^\\:]+(?=\.))({file_ext}\.[^\\:]+?)?|[^\\:]+?)\s*ハンドル ID:""",
    """プロセス名:\s*({process_path}({process_dir}.+?[\\\/])?({process_name}[^\\\/"]+?))\s*アクセス要求情報:""",
    """アクセス:\s*({access}.+?)\s*アクセス マスク:""",
  ]
  DupFields = [ "host->dest_host"]


}
```