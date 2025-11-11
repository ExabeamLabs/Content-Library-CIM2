#### Parser Content
```Java
{
Name = secureauth-idp-kv-endpoint-authentication-fail-51140
  Product = SecureAuth IDP
  ParserVersion = "v1.0.0"
  Conditions = [ """EventID="51140"""", """RequestID=""", """BrowserSession=""", """PEN=""", """Appliance=""" ]
  Fields = ${SecureAuthDLParsersTemplates.secure-auth-events.Fields} [
    """\WEventID="[^\]]*?\]\s({failure_reason}[^"]+)\s*"*$""",
    """Message="\s*({failure_reason}[^"]+)\s*""""
  ]

secure-auth-events = {
  Vendor = SecureAuth
  Product = SecureAuth Login
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields =[
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s""",
    """Timestamp="({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",
    """\WUserHostAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WRealm="({realm}[^"]+)""",
    """\WAppliance="({host}({dest_host}[\w\-.]+))""",
    """\WHostName ="({host}[\w\-.]+)"""",
    """\WUserID="(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
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