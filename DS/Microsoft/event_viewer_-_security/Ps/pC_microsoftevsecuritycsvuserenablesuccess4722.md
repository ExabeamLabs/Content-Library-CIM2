#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-user-enable-success-4722
   ParserVersion = v1.0.0
   Vendor = Microsoft
   Product = Event Viewer - Security
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ """4722""", """ユーザー アカウントが有効化されました。""" ]
   Fields = [
     """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4722),""",
     """({host}[\w.\-]+),ユーザー アカウントが有効化されました。""",
     """アカウント名:\s*({user}[\w\.\-]{1,40}\$?)\s*アカウント ドメイン:\s*({domain}.*?)\s*ログオン ID:\s*({login_id}.*?)\s*ターゲット.+?アカ>ウント名:\s*({dest_user}.*?)\s*アカウント ドメイン:\s*({dest_domain}.*?)\s*($|")"""
   ]
   DupFields = [ "host->dest_host" ]


}
```