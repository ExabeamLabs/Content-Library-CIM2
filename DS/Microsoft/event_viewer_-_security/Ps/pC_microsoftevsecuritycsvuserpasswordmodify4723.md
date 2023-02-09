#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-user-password-modify-4723
   ParserVersion = v1.0.0
   Vendor = Microsoft
   Product = Event Viewer - Security
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ """4723""", """アカウントのパスワードの変更が試行されました。""" ]
   Fields = [
     """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4723),""",
     """({host}[\w.\-]+),アカウントのパスワードの変更が試行されました。""",
     """アカウント名:\s*({user}.*?)\s*アカウント ドメイン:\s*({domain}.*?)\s*ログオン ID:\s*({login_id}.*?)\s*ターゲット.+?セキ>ュリティ ID:\s*({dest_user_sid}.*?)\s*アカウント名:\s*({dest_user}.*?)\s*>アカウント ドメイン:\s*({dest_domain}.*?)\s*追加情報"""
   ]
   DupFields = [ "host->dest_host" ]


}
```