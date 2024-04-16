#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-4768-5
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """ 4768 """, """已要求 Kerberos 驗證票證 (TGT)。""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3})""",
    """\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}[\-\+]\d\d:\d\d ({host}[\w.\-]+)\s""",
    """(Information|Audit Success|Success Audit|Failure Audit|Audit Failure)\s*({host}[\w.\-]+?)\s""",
    """({event_code}4768)""",
    """\s帳戶名稱:\s*({user}[\w\.\-]{1,40}\$?)(?:@([^\s]+))?\s""",
    """\s支援領域名稱:\s*({domain}\S+)""",
    """\s使用者識別碼:\s*(?:NULL SID|({user_sid}.+?))\s*服務資訊:""",
    """\s用戶端位址:\s*(::[\w]+:)?({src_ip}(?!::1)((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\s結果碼:\s*({result_code}[\w\-]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```