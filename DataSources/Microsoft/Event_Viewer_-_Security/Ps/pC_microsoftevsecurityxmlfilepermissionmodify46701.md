#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-file-permission-modify-4670-1
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4670<""", """Permissions on an object were changed""", """<Data Name\=""", """ObjectServer""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-3.Fields}[
    """({event_name}Permissions on an object were changed)""",
    """<Data Name\\='HandleId'>({object_id}[^<]+)<""",
    """<Data Name\\='ObjectServer'>(-|({object_server}[^<]+))<""",
    """<Data Name\\='ObjectType'>(-|({object_type}[^<]+))<""",
    """<Data Name\\='ObjectName'>(-|({object}[^<]+))<""",
    """<Data Name\\='OldSd'>({old_attribute}[^<]+)<""",
    """<Data Name\\='NewSd'>({new_attribute}[^<]+)<"""
  ]
  DupFields = ["process_name -> file_name"]

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