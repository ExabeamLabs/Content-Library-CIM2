#### Parser Content
```Java
{
Name = fireeye-endpointsecurity-str-endpoint-notification-success-wsmd-1
  ParserVersion = "v1.0.0"
  Conditions = [ """ wsmd[""", """]: """, """trellix""" ]

fireeye-endpointsecurity-hx-events = {
  Vendor = Trellix
  Product = Trellix Endpoint Security (HX)
  TimeFormat = "MMM dd HH:mm:ss"
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s""",
    """(\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s[\w\-\.]+\s[\w-]+\[({event_code}\d+)\]""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\S+\s\S+\s\[?(\w+\.)?({severity}(?i)(NOTICE|ERR(OR)?|WARNING))\]?:?""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\S+\s\S+\s(\[[^\]]+\]:)?\s*({additional_info}[^$]+?)\s*$""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\S+\s({event_name}[^\[:]+)(\[|:)"""
    """\suser(name)?\s'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """,\srole\s'({role}[^']+)'""",
    """,\srequest:\s"({method}[^\s]+)\s({uri_path}\/[^\s\?]*?)?({uri_query}\?[^\s]+)?\s({protocol}[^\/]+)\/""",
    """:\ssession\s({session_id}\d+)"""
  
}
```