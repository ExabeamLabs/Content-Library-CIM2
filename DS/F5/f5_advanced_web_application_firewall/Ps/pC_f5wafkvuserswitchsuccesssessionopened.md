#### Parser Content
```Java
{
Name = f5-waf-kv-user-switch-success-sessionopened
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """session opened for user""", """(uid=""", """sshd:""", """_unix""" ]
  Fields = ${F5ParsersTemplates.f5-waf-activity.Fields} [
    """\(uid=({user_uid}\d+)\)""",
    """session opened for user ({dest_user}[^\s]+) by""",
    """sshd\[({login_id}\d+)""",
    """({event_code}ssh)""",
  ]
  ParserVersion = "v1.0.0"

f5-waf-activity = {
    Vendor = F5
    Product = F5 Advanced Web Application Firewall
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"host":"(::ffff:)?({host}[^"]+})""",
      """\d\d:\d\d:\d\d ({host}\S+)? \w+ \w+\[""",
      """\ssshd\[\d+\]:\s*({additional_info}[^",]+)"""
    
}
```