#### Parser Content
```Java
{
Name = unix-unix-str-alert-trigger-sshdbreakinattempt
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """POSSIBLE BREAK-IN ATTEMPT!""", """ sshd[""" ]
  Fields = [
    """({alert_name}POSSIBLE BREAK-IN ATTEMPT!)""",
    """ Address ({src_ip}[a-fA-F\d.:]+) maps to ({src_host}[^,]+)""",
    """({host}[\w.\-]+) ({process_name}sshd)\[""",
    """({additional_info}Address .+?- POSSIBLE BREAK-IN ATTEMPT!)\s*$"""
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```