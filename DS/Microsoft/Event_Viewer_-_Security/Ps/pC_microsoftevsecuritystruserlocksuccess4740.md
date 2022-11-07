#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-user-lock-success-4740
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """4740""", """ユーザー アカウントがロックアウトされました。""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}4740),""",
    """({host}[\w.\-]+),ユーザー アカウントがロックアウトされました。""",
    """サブジェクト.+?\s*アカウント名:\s*({caller_user}.*?)\s*アカウント ドメイン:\s*({caller_domain}.*?)\s*ログオン ID:\s*({login_id}.*?)\s*ロックアウトされたアカウント.+?セキュリティ ID:\s*({user_sid}.*?)\s*アカウント名:\s*({user}.*?)\s*追加情報:.+?呼び出し元コンピューター名:\s*({src_host}.*?)\s*("|$)"""
    ]
   DupFields = [ "host->dest_host", "caller_domain->domain" ]


}
```