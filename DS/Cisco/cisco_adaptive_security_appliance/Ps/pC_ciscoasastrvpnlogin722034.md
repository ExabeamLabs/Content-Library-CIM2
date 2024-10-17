#### Parser Content
```Java
{
Name = "cisco-asa-str-vpn-login-722034"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """-722034""", """%ASA-""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)(\s+({host}[\w\-.]+)\s*)?""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """\sGroup\s*<({group_name}.+?)>""",
    """\sUser\s*<({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^>]+))?>""",
    """\sIP\s*<(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))>""",
    """\s*({event_name}New\s({protocol}\w+)\s+SVC connection)"""
  ]


}
```