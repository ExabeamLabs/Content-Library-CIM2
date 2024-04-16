#### Parser Content
```Java
{
Name = ivanti-ps-str-vpn-login-success-sessionstarted
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""PulseSecure: """
"""Session started for User """
"""app_session_id"""
]
  Fields = [
    """\s({host}[\w\-\.]+)\s*PulseSecure:""",
    """PulseSecure:.+?-\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*-\s*[^\s]+\s*-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\s({user}[\w\.\-]+)\(({realm}[^\)]+)\)"""
    """({event_name}Session started for User) \[({user}[^\]]+)\]\swith app_session_id \[({session_id}[^\]]+)"""
    ]


}
```