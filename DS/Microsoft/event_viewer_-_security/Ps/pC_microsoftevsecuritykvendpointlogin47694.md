#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-4769-4
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""A Kerberos service ticket was requested""", """Account Name""", """Computer"""]
  Fields = [
    """({event_name}A Kerberos service ticket was requested)""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
    """<Computer>({host}[^<]+)</Computer>""",
    """Computer(\w+)?["\s]*(:|=)\s*"?({host}.+?)("|\s|;)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_code}4769)""",
    """Account Name(:|=)\s*(\w+\/({src_host}[^@\s]+)(@({domain}[\w._\-]+))?|({user}[^@:\s;]+)(@({=domain}[\w._\-]+))?)[\s;]*Account Domain(:|=)""",
    """Account Domain(:|=)\s*({domain}[^\\:=]+?)[\n\s;]*Logon GUID(:|=)""",    
    """Service Name(:|=)\s*({dest_host}[^\\\s;]+\$)[\n\s;]*Service ID""",
    """Service Name(:|=)\s*({service_name}[^\\\s;]+)[\n\s;]*Service ID""",
    """Client Address(:|=)\s*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Failure Code(:|=)\s*({result_code}.+?)[\\n\s;]*Transited Services(:|=)""",
    """Ticket Options(:|=)\s*({ticket_options}.+?)[\n\s;]*Ticket Encryption Type(:|=)"""
    """Ticket Encryption Type(:|=)\s*({ticket_encryption_type}.+?)[\n\s;]*Failure Code(:|=)"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```