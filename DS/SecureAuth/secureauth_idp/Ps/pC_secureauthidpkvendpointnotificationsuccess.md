#### Parser Content
```Java
{
Name = secureauth-idp-kv-endpoint-notification-success
  Vendor = SecureAuth
  Product = SecureAuth IDP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """EventID="""", """Priority="""", """PEN="""", """Category="""", """HostName ="""" ]
  Fields =[
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s""",
    """Timestamp="({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",
    """\WUserHostAddress="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WRealm="({realm}[^"]+)""",
    """\WAppliance="({host}({dest_host}[\w\-.]+))""",
    """\WHostName ="({host}[\w\-.]+)"""",
    """\WUserID="(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[^"]+))"""",
    """\WPriority="({priority}\d+)""",
    """\WEventID="({event_code}\d+)""",
    """UserAgent="(?:-|Mozilla\/.+({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin).+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))""",
    """UserAgent="({user_agent}[^"]+)"""",
    """\WEventID="[^\]]*?\]\s({additional_info}[^"]+)\s*"*$""",
    """Message="\s*({additional_info}[^"]+)\s*"""",
    """\WCategory="({category}[^"]+)""""
  ]
 

}
```