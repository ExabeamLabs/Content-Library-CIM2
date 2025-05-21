#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-ds-object-modify-success-5136-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [ "|Snare|", "A directory service object was modified"]
  Fields = [
    """({event_name}A directory service object was modified)""",
    """({event_code}5136)""",
    """\Wrt=({time}\d{13})""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdhost=({src_host}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
    """\Wdvchost=({host}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdntdom=({domain}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
    """\Wduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
    """\Wduid=({login_id}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
    """\WcategoryOutcome=\/?({result}.+?)\s+(\w+=|$)""",
    """\Wcs5=(|({object_type}.+?))(\s+(\w+|\w+\.\w+)=|\s*$)""",
    """\Wcs6=(|({ds_object_dn}.+?))(\s+(\w+|\w+\.\w+)=|\s*$)""",
    """\Wcs6=(|[^=]*?({ds_object_ou}OU.+?))(\s+(\w+|\w+\.\w+)=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```