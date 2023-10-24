#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-file-permission-modify-4670-1
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4670<""", """Permissions on an object were changed""", """<Data Name\=""", """ObjectServer""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-3.Fields}[
    """({event_name}Permissions on an object were changed)""",
    """<Data Name\\=('|")HandleId('|")>({object_id}[^<]+)<""",
    """<Data Name\\=('|")ObjectServer('|")>(-|({object_server}[^<]+))<""",
    """<Data Name\\=('|")ObjectType('|")>(-|({object_type}[^<]+))<""",
    """<Data Name\\=('|")ObjectName('|")>(-|({object}[^<]+))<""",
    """<Data Name\\=('|")OldSd('|")>({old_attribute}[^<]+)<""",
    """<Data Name\\=('|")NewSd('|")>({new_attribute}[^<]+)<"""
  ]
  DupFields = ["process_name -> file_name"]

windows-events-3 = {
      Vendor = Microsoft
      Product = Event Viewer - Security
      TimeFormat = "epoch"
      Fields = [
        """\Wrt=({time}\d{13})""",
        """\sagt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """\Wdhost=\s*({dest_host}[\w\-.]+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\sahost=({host}[^\s]+)""",
        """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
        """\Wdntdom=({domain}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wduser=\s*((?i)local service|({user}[\w\.\-]{1,40}\$?)|({full_name}[^"=]+))(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wduid=(-|({login_id}[^=]+))\s\w+=""",
        """\WfilePath=(?:[\\\*]+)?({share_name}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\Wad\.ShareLocalPath=(?:[\\\?]+)?(?:\s*|({share_path}({d_parent}.*?)({d_name}[^\\]+?))(\\+)?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
        """\said=({aid}[^\s\\]+)""",
        """categoryOutcome=\/({result}[^\s]+)"""
        """Source Port(=|:)\s*({src_port}\d+)"""
        
}
```