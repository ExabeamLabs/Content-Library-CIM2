#### Parser Content
```Java
{
Name = ivanti-ps-str-vpn-logout-success-notauthenticated
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""PulseSecure: """
"""Connection from """
"""not authenticated yet """
]
  Fields = [
    """\s({host}[\w\-\.]+)\s*PulseSecure:""",
    """PulseSecure:.+?-\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*-\s*[^\s]+\s*-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\(({realm}[^\)]+)\)""",
    """Connection from IP ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """\(URL=({url}[^\)]+)\)"""
    ]


}
```