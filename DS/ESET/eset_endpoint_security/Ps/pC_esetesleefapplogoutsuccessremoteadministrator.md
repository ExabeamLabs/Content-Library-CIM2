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
      """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """srcPort=({src_port}\d+)""",
      """dstPort=({dest_port}\d+)""",
      """\|ESET\|(?:[^\|]+\|){2}({event_name}[^\|]+)""",
      """actionTaken=({action}[^=]+?)\s*(\w+=|$)""",
      """\Wresult=({result}[^=]+?)\s*(\w+=|$)""",
      """\WdeviceName =({device_id}[^\s]+)\s""",
      """\Wdetail=({additional_info}[^.]+)\.""",
      """\Wuser '(({domain}[^\s\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'.""",
      """\Wuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\w+=|$)""",
    ]
  ParserVersion = "v1.0.0"


}
```