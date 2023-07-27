#### Parser Content
```Java
{
Name = rsa-securid-kv-vpn-logout-success-sessionremoved
  Vendor = RSA
  Product = SecurID
  TimeFormat = "EEE MMM dd HH:mm:ss z yyyy"
  Conditions = [ """USER_SESSION_REMOVED_TIMEOUT""", """SESSION_ID=""" ]
  Fields = [
    """<\d+>\w+ \d+ \d+:\d+:\d+ ({host}[\w.\-]+)""",
    """\sUSER_AGENT="({user_agent}[^"]+)""",
    """\sSESSION_INACTIVITY_TIMEOUT="({time}\w+ \w+ \d+ \d+:\d+:\d+ \w+ \d\d\d\d)""",
    """\sUSERNAME="({user}[\w\.\-]{1,40}\$?)""",
    """\sREMOTE_IP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sSESSION_ID="({session_id}[^"]+)""",
    """\sREASON="({result_reason}[^"]+)""",
    """({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s+\S+){2}\s+USER_SESSION_REMOVED_TIMEOUT"""
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = "v1.0.0"


}
```