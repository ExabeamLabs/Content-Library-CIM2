#### Parser Content
```Java
{
Name = microsoft-windows-cef-process-create-success-snare
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Snare|""", """|A new process has been created|""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """CEF:([^\|]*\|){4}Security:({event_code}\d+)\|({event_name}[^\|]+)""",
    """\scategoryBehavior=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\scategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)""",
    """\scategoryObject=(|({object}.+?))(\s+\w+=|\s*$)""",
    """\sdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\sdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\ssrc=({src_ip}[a-fA-F\d.:]+)""",
    """\sduser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\sdproc=(|({process_path}(({process_dir}[^=]*?)[\\\/]+)?({process_name}[^=\\\/]+)))(\s+\w+=|\s*$)""",
    """Process ID\\=({process_id}\d+)""",
    """User\\=(-|({user}[^=&]+))""",
    """ComputerName\\=({host}[\w.\-]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```