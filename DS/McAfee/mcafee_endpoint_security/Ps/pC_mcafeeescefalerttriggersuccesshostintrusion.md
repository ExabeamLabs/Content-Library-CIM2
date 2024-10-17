#### Parser Content
```Java
{
Name = mcafee-es-cef-alert-trigger-success-hostintrusion
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """|McAfee|Host Intrusion Prevention|""" ]
    Fields = [
      """CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|""",
      """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)\|""",
      """\Wcat=({alert_type}.+?)\s+(\w+=|$)""",
      """\Wrt=({time}\d{13})""",
      """\Wshost=({src_host}.+?)\s+(\w+=|$)""",
      """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\Wsuser=(?!NT AUTHORITY)(({domain}[^\\\/=]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?<!SYSTEM)\s+(\w+=|$)""",
      """\Wsproc=({process_path}({process_dir}.*?)[\\\/]*({process_name}[^\\\/=]+?))\s+(\w+=|$)""",
      """\Wdhost=({dest_host}.+?)\s+(\w+=|$)""",
      """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\Wrequest=({malware_file_name}file:.+?)\s+(\w+=|$)""",
      """\Wrequest=(?!file:)({malware_url}.+?)\s+(\w+=|$)""",
      """\Wdvc=({host}.+?)\s+(\w+=|$)""",
      """\Wdvchost=({host}.+?)\s+(\w+=|$)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```