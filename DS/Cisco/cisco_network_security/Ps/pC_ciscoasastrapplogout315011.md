#### Parser Content
```Java
{
Name = cisco-asa-str-app-logout-315011
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """-315011""", """%ASA-""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d)""",
    """%ASA-({priority}\d+)""",
    """({event_code}315011)""",
    """({event_name}disconnected by SSH server)""",
# trust_point is removed
    """from\s*(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """interface\s*({interface}[^\s]+)\s*for""",
    """ user "(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """\s(::ffff:)?(-|({host}[\w\.-]+))[\s:]+%ASA-"""
  ]


}
```