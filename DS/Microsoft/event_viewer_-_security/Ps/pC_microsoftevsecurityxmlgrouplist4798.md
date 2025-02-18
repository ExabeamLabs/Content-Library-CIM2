#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-list-4798
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4798<""", """Microsoft-Windows-Security-Auditing""", """<Data Name\=""", """TargetUserName""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-3.Fields}[
    """<Computer>({host}[^<>]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_name}A user's local group membership was enumerated)""",
    """<Level>({run_level}[^<]+)<"""
  ]

windows-events-3 = {
      Vendor = Microsoft
      Product = Event Viewer - Security
      TimeFormat = "epoch"
      Fields = [
        """\Wrt=({time}\d{13})""",
        """\sagt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
        """\Wdntdom=({domain}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wduser=\s*((?i)local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"=]+))(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wduid=(-|({login_id}[^=]+))\s\w+=""",
        """\WfilePath=(?:[\\\*]+)?({share_name}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wad\.ShareLocalPath=(?:[\\\?]+)?(?:\s*|({share_path}({d_parent}.*?)({d_name}[^\\]+?))(\\+)?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\said=({aid}[^\s\\]+)""",
        """categoryOutcome=\/({result}[^\s]+)"""
        """Source Port(=|:)\s*({src_port}\d+)"""
        
}
```