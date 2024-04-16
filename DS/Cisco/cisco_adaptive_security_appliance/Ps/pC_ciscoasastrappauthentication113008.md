#### Parser Content
```Java
{
Name = cisco-asa-str-app-authentication-113008
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """%ASA-""", """-113008""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)\s*\S*\s*:\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """-113008:\s+({event_name}AAA transaction status ACCEPT)""",
    """user\s*=\s*({user}[\w\.\-]{1,40}\$?)(@({domain}[^@,\s:]+))?""",
    """user\s*=\s*(({email_address}[^\@"]+\@[^"|\s]+)|({user}[\w\.\-]{1,40}\$?))"""
    """\d\d:\d\d:\d\d\s+(::ffff:)?((?i)system|({host}[\w\.-]+))[\s:]+%ASA-"""
  ]


}
```