#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-time-modify-4616
    ParserVersion = v1.0.0
    Conditions = [ """CEF:""", """|Microsoft-Windows-Security-Auditing:4616|""", """The system time was changed""" ]
    Fields = ${WindowsParsersTemplates.windows-events-3.Fields} [
      """\Wdhost=\s*({dest_host}[\w\-.]+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
      """\sahost=({host}[^\s]+)""",
      """({event_name}The system time was changed)""",
      """({event_code}4616)""",
	  """ad\.ProcessID=({process_id}\d+)""",
	  """ad\.ThreadID=({thread_id}\d+)""",
	  """dproc=({process_path}({process_dir}[^=]+)\\({process_name}[^=]+))\s\w+="""
	  
   ]

windows-events-3 = {
      Vendor = Microsoft
      Product = Event Viewer - Security
      TimeFormat = "epoch"
      Fields = [
        """\Wrt=({time}\d{13})""",
        """\sagt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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