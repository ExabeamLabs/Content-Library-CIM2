#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-leef-app-activity-protection
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = Carbon Black App Control
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [ """LEEF:""", """|Carbon_Black|Protection|"""]
  Fields = [
    """({host}[\w\-.]+)\s+LEEF:""",
    """\WdevTime=({time}\w+\s+\d+\s+\d\d\d\d\s+\d\d:\d\d:\d\d\.\d+ \w+)""",
    """\WreceivedTime=({received_time}\w+\s+\d+\s+\d\d\d\d\s+\d\d:\d\d:\d\d\.\d+ \w+)""",
    """\Wcat=(|({category}.+?))\s+(\w+=|$)""",
    """\Wsev=({alert_severity}\d+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WsrcHostName =(({domain}[^\\\s]+)\\+)?({src_host}[\w\-.]+)""",
    """\WsrcProcess=(|({process_path}({process_dir}[^,]*?)(\\+({process_name}[^\\,]+?))?))\s+(\w+=|$)""",
    """\WusrName =(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\WfilePath=(|({file_path}(({file_dir}[^=,]+[^\\])\\+)?({file_name}[^\\,]+?)))\s+(\w+=|$)""",
    """\WfileName =(|({file_name}[^\/,]+?(\.({file_ext}[^\/,\.]+?))?))\s+(\w+=|$)""",
    """\WfileHash=({old_hash}[^,\s]+)""",
    """\WdstHostName =({dest_host}[\w\-.]+)""",
    """\WinstallerFileName =(|({src_process_name}.+?))\s+(\w+=|$)""",
    """\Wpolicy=(|({policy_name}.+?))\s+(\w+=|$)""",
  ]
  DupFields = [ "old_hash->new_hash" ]


}
```