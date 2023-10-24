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
    """\Wrt=({time}\d{13})""",
    """dvc=({host}[^\s]+)"""
    """src=(AD|Identity|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """act=({action}.+?)\s\w+="""
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
    """categoryOutcome=(\/)?({result}.+?)\s\w+=""",
    """\W(s|d)user=({last_name}[^\s]+)\s+({first_name}[^\s]+)\s+-\s+\(({department}[^)]+)\)\s+-\s+({company}[^\s]+)\s+\((({email_address}[^@\s]+@[^)]+)|({user}[\w\.\-]{1,40}\$?))""",
    """\W(s|d)user=((CheckPoint|({last_name}[^\s]+))\s+(Firewall|({first_name}[^\s]+))\s+)\((({email_address}[^\s@]+@[^\)]+)|checkpointfw|({user}[\w\.\-]{1,40}\$?))""",
  ]


}
```