#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-722033
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ 
  """-722033"""
  """%ASA-""" 
  ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)"""
    """%ASA-({priority}\d+)-({event_code}\d+)"""
    """\sGroup\s*<({group_name}[^>]+)>"""
    """\sUser\s*<(({email_address}[^@]+@[^>]+)|(({domain}[^\\>]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))>""",
    """\sIP\s*<(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([^:]+?:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+))>"""
    """({event_name}First\s*(TCP|UDP|)\s*SVC connection established for SVC session)"""
    """({protocol}SVC)"""
    """\s(::ffff:)?(-|({host}[\w\.-]+))[\s:]+%ASA-"""
  ]


}
```