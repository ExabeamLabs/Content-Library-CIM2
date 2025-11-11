#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-lock-success-4740-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ "EventIDCode=4740"]
  Fields = [
    """\s+Computer=({host}[\w.\-]+)""",
    """EventIDCode=({event_code}\d+)""",
    """Message=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({src_host}[^\s]+)\s({user_sid}[^\s]+)\s(.+?)\s({src_user}[^\s]+)\s({domain}({src_domain}[^\s]+))\s({login_id}[^\s]+)\s*$"""
  ]


}
```