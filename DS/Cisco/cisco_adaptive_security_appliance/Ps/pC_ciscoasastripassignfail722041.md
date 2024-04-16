#### Parser Content
```Java
{
Name = cisco-asa-str-ip-assign-fail-722041
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-722041""", """TunnelGroup """ ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """\d\d:\d\d:\d\d\s+(::ffff:)?((?i)system|({host}[\w\.-]+))[\s:]+%ASA-""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """ User <(({domain}[^\s\\]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))>""",
    """\sIP\s+<({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>""",
    """ Group\s+<({realm}.+?)>""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d).*?%ASA-""",
    """\sGroup\s*<({group_name}[^>]+)>""",
    """\sUser\s*<({user}[\w\.\-]{1,40}\$?)>""",
    """({failure_reason}No IPv6 address available for SVC connection)"""

  ]
}, 

{
  Name = cisco-asa-str-network-session-fail-requestdiscarded
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """%ASA""", """-710005""", """request discarded""" ]
  Fields = [
        """({time}\w+\s\d\d\s\d{0,4}\s*\d\d:\d\d:\d\d)""",
        """%ASA-({priority}\d+)-({event_code}\d+)""",
        """%ASA-[^\s]+\s({protocol}\w+)""",
        """({action}request ({result}discarded))""",
        """\sfrom\s+({src_ip}[.:a-fA-F\d]+)\/({src_port}\d+)""",
        """\sto\s\S+\:({dest_ip}[.:a-fA-F\d]+)\/({dest_port}\d+)""",
  ]


}
```