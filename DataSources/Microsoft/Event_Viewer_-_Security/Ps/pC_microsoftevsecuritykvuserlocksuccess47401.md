#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-lock-success-4740-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [ "EventIDCode=4740"]
  Fields = [
    """\s+Computer=({dest_host}[\w.\-]+)""",
    """EventIDCode=({event_code}\d+)""",
    """Message=({user}[^\s]+)\s({src_host}[^\s]+)\s({user_sid}[^\s]+)\s(.+?)\s({caller_user}[^\s]+)\s({caller_domain}[^\s]+)\s({login_id}[^\s]+)\s*$"""
  ]
  DupFields = ["caller_domain->domain"]


}
```