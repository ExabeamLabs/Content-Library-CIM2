#### Parser Content
```Java
{
Name = cisco-asa-kv-vpn-logout-611103
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ 
  """%ASA-"""
  """-611103""" 
  ]
  Fields = ['
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)\s*(({host}[\w.\-]+))?\s*:\s*%ASA\-({priority}\d+)\-({event_code}\d+)"""
    """-611103:\s*({event_name}User logged out)"""
    """Uname:\s*({user}[\w\.\-]{1,40}\$?)"""
    """\d\d:\d\d:\d\d\s+(::ffff:)?((?i)system|({host}[\w\.-]+))[\s:]+%ASA-"""
    ]


}
```