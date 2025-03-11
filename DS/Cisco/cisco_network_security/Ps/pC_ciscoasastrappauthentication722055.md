#### Parser Content
```Java
{
Name = cisco-asa-str-app-authentication-722055
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """ Client Type:""", """-722055""", """: Group <""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%\w+""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%\w+\-({priority}\d+)\-({event_code}\d+)""",
    """Group <({group_name}[^>]+)>""",
    """\sUser\s*<(({email_address}[^@\s>]+@[^>\s\.]+\.[^>\s]+)|((({domain}[^\\>]+)[\/\\])?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))>""",
    """IP <(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """({event_name}AnyConnect VPN Agent for ({os}[^"]+?))\s\d"""
    """Client Type:\s*({user_agent}[^":\n]+)"""
    """\s(::ffff:)?(-|({host}[\w\.-]+))[\s:]+%\w+-"""
  ]
  DupFields = [ "group_name->realm" ]


}
```