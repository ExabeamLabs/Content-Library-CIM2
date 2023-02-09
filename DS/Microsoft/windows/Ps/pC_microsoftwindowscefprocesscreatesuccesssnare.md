#### Parser Content
```Java
{
Name = microsoft-windows-cef-process-create-success-snare
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Snare|""", """|A new process has been created|""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """CEF:([^\|]*\|){4}Security:({event_code}\d+)\|({event_name}[^\|]+)""",
    """\scategoryBehavior=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\scategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)""",
    """\scategoryObject=(|({object}.+?))(\s+\w+=|\s*$)""",
    """\sdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sduser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\sdproc=(|({process_path}(({process_dir}[^=]*?)[\\\/]+)?({process_name}[^=\\\/]+)))(\s+\w+=|\s*$)""",
    """Process ID\\=({process_id}\d+)""",
    """User\\=(-|({user}[^=&]+))""",
    """ComputerName\\=({host}[\w.\-]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```