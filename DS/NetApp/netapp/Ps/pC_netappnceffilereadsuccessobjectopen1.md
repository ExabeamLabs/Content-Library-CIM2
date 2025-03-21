#### Parser Content
```Java
{
Name = netapp-n-cef-file-read-success-objectopen-1
  Product = NetApp
  Conditions = [ """|NetApp|NetApp-Security-Auditing|""", """|Open Object|""" ]
  ParserVersion = "v1.0.0"

cef-netapp-file-operations = {
  Vendor = NetApp
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wahost=({host}[A-Fa-f:\d.]+)""",
    """\Wahost=({host}[\w\-.]+)""",
    """\Wapp=({app}[^\s]+)\s""",
    """\Wcat=({category}[^\s]+)\s""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s""",
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