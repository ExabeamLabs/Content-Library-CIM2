#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-authentication-unauthenticatedrequest
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ PulseSecure: - - ""","""- Unauthenticated request url """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s\S+\s\S+\s\S+\s\[({host}[\w\-.]+)\]\s(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\sHost:\s*({host}[\w\-.]+)\s""",
    """\s({host}[\w\-.]+)\s+PulseSecure:""",
    """({operation}Unauthenticated request url)""",
    """Unauthenticated request url\s({uri_path}\/[^\?\s]*?)(\?({uri_query}\S+))?\s""",
    """IP\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({app}PulseSecure)""",
    """\sUser-Agent:\s*({user_agent}.+?)\s[\w\-\.]+:"""
  ]
  ParserVersion = "v1.0.0"


}
```