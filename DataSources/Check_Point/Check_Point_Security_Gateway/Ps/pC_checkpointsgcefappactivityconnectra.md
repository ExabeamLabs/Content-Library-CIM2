#### Parser Content
```Java
{
Name = checkpoint-sg-cef-app-activity-connectra
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point Security Gateway
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Check Point|"""]
  Fields = [
    """\Wrt=({time}\d+)""",
    """dvc=({host}[^\s]+)"""
    """src=(AD|Identity|({src_ip}[^\s]+))""",
    """dst=({dest_ip}[^\s]+)"""
    """act=({action}.+?)\s\w+="""
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
    """categoryOutcome=(\/)?({result}.+?)\s\w+=""",
    """\W(s|d)user=({last_name}[^\s]+)\s+({first_name}[^\s]+)\s+-\s+\(({department}[^)]+)\)\s+-\s+({company}[^\s]+)\s+\((({email_address}[^@\s]+@[^)]+)|({user}[^\)]+))""",
    """\W(s|d)user=((CheckPoint|({last_name}[^\s]+))\s+(Firewall|({first_name}[^\s]+))\s+)\((({email_address}[^\s@]+@[^\)]+)|checkpointfw|({user}[^\)]+))""",
  ]


}
```