#### Parser Content
```Java
{
Name = netapp-n-cef-file-write-success-cifs
  Product = NetApp
  Conditions = [ """|NetApp|NetApp-Security-Auditing|""", """CEF:""", """app=CIFS"""]
  ParserVersion = "v1.0.0"

cef-netapp-file-operations = {
  Vendor = NetApp
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wahost=({host}[A-Fa-f:\d.]+)""",
    """\Wahost=({host}[\w\-.]+)""",
    """\Wapp=({app}[^\s]+)\s""",
    """\Wcat=({category}[^\s]+)\s""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wsuser=({user}[^\s]+)\s""",
    """\Wfname=({file_path}.+?)\s*(\w+=|$)""",
    """\Wfname=.*?({file_name}[^\\]+?)\s*(\w+=|$)""",
    """\Wfname=.*?(\.({file_ext}[^\\\.]+?))?\s*(\w+=|$)""",
    """\WfileId=(-|({file_id}\d+))""",
    """filePath=({file_path}({file_dir}.+?)([\\\/]*({file_name}[^\\\/]+?))?)\s+(\w+=|$)""",
    """\WfileType=({file_type}.+?)\s*(\w+=|$)""",
    """CEF:([^\|]*\|){5}({access}[^\|]+)""",
    """\Wcs1=(-|({user_sid}.+?))\s*(\w+=|$)""",
    """\Woutcome=.+({result}Success|Failure)""",
    """CEF:([^\|]*\|){6}((?i)unknown|({severity}[^\|]+))""",
    """filePermission=({file_permissions}.+?)\s*cs1""",
  ]
 
}
```