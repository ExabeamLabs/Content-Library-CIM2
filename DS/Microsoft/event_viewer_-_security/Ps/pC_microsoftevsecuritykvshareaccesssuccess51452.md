#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-success-5145-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """5145""", """クライアントに必要なアクセスを付与できるかどうかについて、ネットワーク共有オブジェクトが>チェックされました。""" ]
  Fields = [
    """\sTimeGenerated=({time}\d+)""",
    """情報,({time}\d\d\d\d\/\d\d\/\d\d \d+:\d\d:\d\d),Microsoft-Windows-Security-Auditing,({event_code}\d+)""",
    """({event_name}[^,]+),"*({additional_info}[^,"]+)\s+$""",
    """\sアクセス:\s*({access}[^\s:]+)\s""",
    """\sMessage=({event_name}\S+)""",
    """\sセキュリティ ID:\s*({user_sid}[^:]+?)\s*アカウント名:""",
    """\sアカウント名:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*アカウント ドメイン:""",
    """\sアカウント ドメイン:\s*({domain}[^:]+?)\s*ログオン ID:""",
    """\sログオン ID:\s*({login_id}\S+)""",
  ]


}
```