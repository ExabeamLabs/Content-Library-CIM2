#### Parser Content
```Java
{
Name = cisco-cucs-str-endpoint-login-fail-authfailed
  Vendor = Cisco
  Product = Cisco IOS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy MMM dd HH:mm:ss zzz"
  Conditions = [ """Authentication failed for User:""", """%USER-2-SYSTEM_MSG:""" ]
  Fields = [
    """\s({host}[a-fA_F0-9.:]+)\s+:""",
    """\s({dest_ip}[a-fA_F0-9.:]+)\s+:"""
    """({time}\d{4}\s\w{3}\s\d{2}\s(\d{2}:){2}\d{2}\s\S+?):""",
    """Authentication failed for User:\s+({user}\S+)\s""",
    """({event_name}Authentication failed for User):"""
  ]


}
```