#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4776-5"
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ " 4776 ", """電腦嘗試驗證帳戶的認證""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3})""",
    """\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}[\-\+]\d\d:\d\d ({host}[\w.\-]+)\s""",
    """\d{2}:\d{2}:\d{2} ({host}[\w.\-]+)\s""",
    """({event_code}4776)""",
    """\s登入帳戶:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@\s]+?))?\s""",
    """\s來源工作站:\s*({src_host}\S+?)\s""",
    """\s錯誤碼:\s*({result_code}[\w\-]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```