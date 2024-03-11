#### Parser Content
```Java
{
Name = cisco-asa-str-ip-assign-fail-722041
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%ASA-""", """-722041""", """TunnelGroup """ ]
  Fields = [
    """\s.*?({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+%ASA-""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """\sUser\s+<(({domain}[^\\]+)\\)?({user}[^>]+)>""",
    """\sIP\s+<({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>""",
    """ Group\s+<({realm}.+?)>""",
  ]
}, 

{
  Name = cisco-asa-str-network-session-fail-requestdiscarded
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA""", """-710005""", """request discarded""" ]
  Fields = [
        """({time}\w+\s\d\d\s\d{4}\s\d\d:\d\d:\d\d)""",
        """%ASA-({priority}\d+)-({event_code}\d+)""",
        """%ASA-[^\s]+\s({protocol}\w+)""",
        """({action}request ({result}discarded))""",
        """\sfrom\s+({src_ip}[.:a-fA-F\d]+)\/({src_port}\d+)""",
        """\sto\s\S+\:({dest_ip}[.:a-fA-F\d]+)\/({dest_port}\d+)""",
  ]


}
```