#### Parser Content
```Java
{
Name = checkpoint-sg-cef-vpn-logout-success-logout
  Vendor = Check Point 
  Product = Security Gateway
  TimeFormat = "epoch"
  Conditions = [ """|Check Point|Connectra|""", """|logout|""" ]
  Fields = [
    """\srt=({time}\d+)(\s+[\w\.:]+=|$)""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\s+[\w\.:]+=|$)""",
    """\sdvchost=({host}.+?)(\s+[\w\.:]+=|$)""",
    """\sduser=({user}.+?)(\s+[\w\.:]+=|$)""",
    """\sduser=[^=]+?\(({user}[^\(\)]+)\)(\s+[\w\.:]+=|$)""",
    """\sshost=({src_host}.+?)(\s+[\w\.:]+=|$)""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\s+[\w\.:]+=|$)""",
    """\sad.duration=({session_duration}.+?)(\s+[\w\.:]+=|$)""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```