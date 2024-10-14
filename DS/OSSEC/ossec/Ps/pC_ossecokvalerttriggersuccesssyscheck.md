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
    """\ssrcip:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """:\sAccepted (publickey|password) for.*?port\s({src_port}\d+)\s""",
    """\saddr=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s""",
    """\sres=({result}[^'"\s;:]+)"""",
    """\sses=({session_id}\d+)""",
    """exe="({process_path}[^"]*)"""",
    """exe="({process_dir}.+\/)({process_name}.+?)"""",
    """\sauid=({account_id}\d+)\s""",
    """\suid=({user_id}\d+)""",
    """op=({action}[^\s]+)""",
    """\suser:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """session opened for user ({dest_user}[^\s]+?)(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_uid}\d+)\))?""",
    """session closed for user\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]
  ParserVersion = "v1.0.0"


}
```