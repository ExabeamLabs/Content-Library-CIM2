#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-user-delete-success-4726
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """4726""", """ユーザー アカウントが削除されました。""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4726),""",
      """({host}[\w.\-]+),ユーザー アカウントが削除されました。""",
      """セキュリティ ID:\s*({user_sid}.*?)\s*アカウント名:\s*({user}.*?)\s*アカウント ドメイン:\s*({domain}.*?)\s*ログオン ID:\s*({login_id}.*?)\s*ターゲット.+?セキュリティ ID:\s*({dest_user_sid}.*?)\s*>アカウント名:\s*({dest_user}.*?)\s*アカウント ドメイン:\s*({dest_domain}.*?)\s*追加情報"""
    ]
    DupFields = [ "host->dest_host", "dest_user->account_name" ]


}
```