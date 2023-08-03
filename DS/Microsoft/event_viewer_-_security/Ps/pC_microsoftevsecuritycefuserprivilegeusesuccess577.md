#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-user-privilege-use-success-577
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Snare|""", """|Security:577|Privileged Service Called|""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """CEF:([^\|]*\|){4}Security:({event_code}\d+)\|({event_name}[^\|]+)""",
    """\scategoryBehavior=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\scategoryresult=(|/({result}.+?))(\s+\w+=|\s*$)""",
    """\scategoryObject=(|({object}.+?))(\s+\w+=|\s*$)""",
    """\sdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sduser=(|SYSTEM|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
    """Primary User Name\\=(-|({user}[^=&]+))""",
    """Primary Domain\\=(-|({domain}[^=&]+))""",
    """Primary Logon ID\\=(-|({login_id}[^=&]+))""",
    """Privileges\\=(-|({privileges}[^=&]+))""",
    """User\\=(SYSTEM|({user}[^=&]+))""",
    """ComputerName\\=({host}[\w.\-]+)""",
  ]


}
```