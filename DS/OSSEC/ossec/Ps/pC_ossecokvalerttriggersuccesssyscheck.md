#### Parser Content
```Java
{
Name = ossec-o-kv-alert-trigger-success-syscheck
  Vendor = OSSEC
  Product = OSSEC
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """ ossec""", """Alert Level:""", """ Location: """, """ classification:""" ]
  Fields = [
    """({time}\w+ \d\d \d\d:\d\d:\d\d)""",
    """\sAlert Level:\s*({alert_severity}\d+)""",
    """\sRule:\s*({alert_name}[^;]+)""",
    """\sLocation:\s*\(({dest_host}[^\)]+)""",
    """Location:(\s*\([^;]*?\))?\s*(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^;\-]+))""",
    """\s(?i)file\s*'({file_path}({file_dir}[^']*?[\\\/]+)?({file_name}[^'\\\/]+?(\.({file_ext}\w+))?))'""",
    """\d\d:\d\d:\d\d\s*({host}[^\s]+)\s*ossec:""",
    """classification:\s*({classification_name}[^,]+)""",
    """\saddr=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s""",
    """\sres=({result}[^'"\s;:]+)"""",
    """\sses=({session_id}\d+)""",
    """exe="({process_path}[^"]*)"""",
    """exe="({process_dir}.+\/)({process_name}.+?)"""",
    """\sauid=({account_id}\d+)\s""",
    """\suid=({user_id}\d+)""",
    """op=({action}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```