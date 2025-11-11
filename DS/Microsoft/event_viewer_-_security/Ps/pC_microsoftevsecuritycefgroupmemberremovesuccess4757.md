#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-group-member-remove-success-4757
    ParserVersion = v1.0.0
    Conditions = [ """CEF:""", """|Microsoft-Windows-Security-Auditing:4757|""", """A member was removed from a security-enabled universal group""" ]
    Fields = ${WindowsParsersTemplates.windows-events-3.Fields} [
      """\sagt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\Wdntdom=({domain}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
      """\Wduser=\s*((?i)local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"=]+))(\s+(\w+|\w+\.\w+)=|\s*$)""",
      """\Wdhost=\s*({dest_host}[\w\-.]+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
      """\sahost=({host}[^\s]+)""",
      """({event_name}A member was removed from a security-enabled universal group)""",
      """({event_code}4757)""",
	  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
	  """duser=({dest_user}[^=]+)\s\w+=""",
	  """sntdom=({domain}[^=\\\s]+)""",
	  """dntdom=({dest_domain}[^=\\\s]+)""",
	  """cs6=(({group_domain}[^\\=]+)\\+)?({group_name}[^=]+?)\s\w+="""
   ]

windows-events-3 = {
      Vendor = Microsoft
      Product = Event Viewer - Security
      TimeFormat = "epoch"
      Fields = [
        """\Wrt=({time}\d{13})""",
        """\Wduid=(-|({login_id}[^=]+))\s\w+=""",
        """\WfilePath=(?:[\\\*]+)?({share_name}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wad\.ShareLocalPath=(?:[\\\?]+)?(?:\s*|({share_path}({d_parent}.*?)({d_name}[^\\]+?))(\\+)?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\said=({aid}[^\s\\]+)""",
        """categoryOutcome=\/({result}[^\s]+)"""
        """Source Port(=|:)\s*({src_port}\d+)"""
        
}
```