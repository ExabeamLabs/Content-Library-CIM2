#### Parser Content
```Java
{
Name = dell-rsaauthmngr-kv-app-logout-success-sessionremoved
  Vendor = RSA
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ SINGLEPOINT """, """ USER_LOGOUT_AFTER_SESSION_REMOVED """ ]
  Fields = [
    """({host}[\w\-.]+) \d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ SINGLEPOINT""",
    """USER_AGENT="(N\/A|({user_agent}[^"]+))""",
    """USERNAME="(N\/A|({user}[\w\.\-]{1,40}\$?))""",
# remote_ip is removed
    """SESSION_ID="(N\/A|({session_id}[^"]+))""",
    """REASON="(N\/A|({result_reason}[^"]+))""",
    """({event_name}USER_LOGOUT_AFTER_SESSION_REMOVED)""",
    """\]\s+({additional_info}User[^"]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```