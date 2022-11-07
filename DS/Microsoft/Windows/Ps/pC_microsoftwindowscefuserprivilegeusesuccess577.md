#### Parser Content
```Java
{
Name = microsoft-windows-cef-user-privilege-use-success-577
  Vendor = Microsoft
  Product = Windows
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Snare|""", """|Security:577|Privileged Service Called|""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """CEF:([^\|]*\|){4}Security:({event_code}\d+)\|({event_name}[^\|]+)""",
    """\scategoryBehavior=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\scategoryresult=(|/({result}.+?))(\s+\w+=|\s*$)""",
    """\scategoryObject=(|({object}.+?))(\s+\w+=|\s*$)""",
    """\sdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\sdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\sduser=(|SYSTEM|({user}.+?))(\s+\w+=|\s*$)""",
    """Primary User Name\\=(-|({user}[^=&]+))""",
    """Primary Domain\\=(-|({domain}[^=&]+))""",
    """Primary Logon ID\\=(-|({login_id}[^=&]+))""",
    """Privileges\\=(-|({privileges}[^=&]+))""",
    """User\\=(SYSTEM|({user}[^=&]+))""",
    """ComputerName\\=({host}[\w.\-]+)""",
  ]


}
```