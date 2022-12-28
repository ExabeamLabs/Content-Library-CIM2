#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-user-disable-success-4725-1
   ParserVersion = v1.0.0
   Vendor = Microsoft
   Product = Event Viewer - Security
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ """4725""", """ユーザー アカウントが無効化されました。""" ]
   Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4725),""",
      """({host}[\w.\-]+),ユーザー アカウントが無効化されました。""",
      """セキュリティ ID:\s*({user_sid}.*?)\s*アカウント名:\s*({user}.*?)\s*アカウント ドメイン:\s*({domain}.*?)\s*ログオン ID:\s*({login_id}.*?)\s*ターゲット.+?セキュリティ ID:\s*({dest_user_sid}.*?)\s*>アカウント名:\s*({dest_user}.*?)\s*アカウント ドメイン:\s*({dest_domain}.*?)\s*("|$)"""
    ]
    DupFields = [ "host->dest_host" ]


}
```