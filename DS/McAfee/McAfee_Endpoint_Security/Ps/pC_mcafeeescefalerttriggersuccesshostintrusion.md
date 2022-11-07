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
      """\Wrt=({time}\d+)""",
      """\Wshost=({src_host}.+?)\s+(\w+=|$)""",
      """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
      """\Wsuser=(?!NT AUTHORITY)(({domain}[^\\\/=]+?)[\\\/]+)?({user}[^=]+?)(?<!SYSTEM)\s+(\w+=|$)""",
      """\Wsproc=({process_path}({process_dir}.*?)[\\\/]*({process_name}[^\\\/=]+?))\s+(\w+=|$)""",
      """\Wdhost=({dest_host}.+?)\s+(\w+=|$)""",
      """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
      """\Wrequest=({malware_file_name}file:.+?)\s+(\w+=|$)""",
      """\Wrequest=(?!file:)({malware_url}.+?)\s+(\w+=|$)""",
      """\Wdvc=({host}.+?)\s+(\w+=|$)""",
      """\Wdvchost=({host}.+?)\s+(\w+=|$)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```