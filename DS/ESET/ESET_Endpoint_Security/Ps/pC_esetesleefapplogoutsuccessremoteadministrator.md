#### Parser Content
```Java
{
Name = eset-es-leef-app-logout-success-remoteadministrator
    Vendor = ESET
    Product = ESET Endpoint Security
    TimeFormat = "MMM dd yyyy HH:mm:ss z"
    Conditions = [ """LEEF:""", """|ESET|RemoteAdministrator|""", """cat=ESET RA Audit Event""", """Native user logout""" ]
    Fields = [
      """\d+Z\s*({host}\w+)\s""",
      """\WdevTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d [^\s]+)""",
      """dst=({dest_ip}[a-fA-F:\d.]+)""",
      """src=({src_ip}[a-fA-F:\d.]+)""",
      """srcPort=({src_port}\d+)""",
      """dstPort=({dest_port}\d+)""",
      """\|ESET\|(?:[^\|]+\|){2}({event_name}[^\|]+)""",
      """actionTaken=({action}[^=]+?)\s*(\w+=|$)""",
      """\Wresult=({result}[^=]+?)\s*(\w+=|$)""",
      """\WdeviceName =({device_id}[^\s]+)\s""",
      """\Wdetail=({additional_info}[^.]+)\.""",
      """\Wuser '(({domain}[^\s\\]+)\\)?({user}[^\s]+)'.""",
      """\Wuser=({user}[^\s=]+?)\s*(\w+=|$)""",
    ]
  ParserVersion = "v1.0.0"


}
```