#### Parser Content
```Java
{
Name = f5-waf-kv-user-switch-success-sessionopened
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """session opened for user""", """(uid=""", """sshd:""", """_unix""" ]
  Fields = ${F5ParsersTemplates.f5-waf-activity-aa.Fields} [
    """\(uid=({user_uid}\d+)\)""",
    """session opened for user ({dest_user}[^\s]+) by""",
    """sshd\[({login_id}\d+)""",
    """({event_code}ssh)""",
  ]
  ParserVersion = "v1.0.0"

f5-waf-activity-aa = {
    Vendor = F5
    Product = F5 Advanced Web Application Firewall
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
      """"host":"(::ffff:)?({host}[^"]+)""",
      """\d\d:\d\d:\d\d ({host}[^\s]+) \w+ \w+\["""
    
}
```