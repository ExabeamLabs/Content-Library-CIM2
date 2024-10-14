#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-network-session-success-5156
  ParserVersion = v1.0.0
  Conditions = [ """,5156,""", """フィルターリング プラットフォームで、接続が許可されました。""" ]

jp-event = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
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
    """Source Port(=|:)\s*({src_port}\d+)"""
  
}
```