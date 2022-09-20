#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-share-access-success-5143
    ParserVersion = v1.0.0
    Conditions = [ """|Microsoft|Microsoft Windows|""", """A network share object was modified""", """Microsoft-Windows-Security-Auditing:5143|""" ]
    Fields = ${WindowsParsersTemplates.windows-events-3.Fields} [
      """({event_name}A network share object was modified)""",
      """({event_code}5143)""",
      ]

windows-events-3 = {
      Vendor = Microsoft
      Product = Event Viewer - Security
      TimeFormat = "epoch"
      Fields = [
        """\Wrt=({time}\d+)""",
        """\sagt=({src_ip}[A-Fa-f0-9.:]+)""",
        """\Wdhost=\s*({dest_host}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\sahost=({host}[^\s]+)""",
        """\Wdst=({dest_ip}[A-Fa-f0-9.:]+)""",
        """\Wdntdom=({domain}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wduser=\s*({user}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wduid=({login_id}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\WfilePath=(?:[\\\*]+)?({share_name}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wad\.ShareLocalPath=(?:[\\\?]+)?(?:\s*|({share_path}({d_parent}.*?)({d_name}[^\\]+?))(\\+)?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\said=({aid}[^\s\\]+)""",
        """categoryOutcome=\/({result}[^\s]+)"""
        
}
```