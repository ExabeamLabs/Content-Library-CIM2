#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-722032
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
  """-722032"""
  """%ASA-""" 
  ]
  Fields = [
    """(Original Address=({host}\S+) )?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)( ({=host}[\w\-.]+))?"""
    """%ASA-({priority}\d+)-({event_code}\d+)"""
    """\sGroup\s*<({group_name}.+?)>"""
    """\sUser\s*<({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^>]+))?>"""
    """\sIP\s*<(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+))>"""
    """({event_name}New\s({protocol}\w+)\s+SVC connection)"""
  ]


}
```