#### Parser Content
```Java
{
Name = cisco-asa-str-user-permission-modify-502103
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ 
  """%ASA-"""
  """-502103""" 
  ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """(({host}[\w\-.]+)\s+)?({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)\s*({=host}[\w\-.]+)?\s*:\s*%ASA\-({priority}\d+)\-({event_code}\d+)"""
    """-502103:\s*({event_name}User priv level changed)"""
    """Uname:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+From"""
# info is removed
]


}
```