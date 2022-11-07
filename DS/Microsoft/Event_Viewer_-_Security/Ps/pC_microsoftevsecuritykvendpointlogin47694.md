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
    """({event_code}4769)""",
    """AccountName(:|=)\s*(\w+\/({src_host}[^@\s]+)(@({domain}[\w._\-]+))?|({user}[^@:\s;]+)(@({=domain}[\w._\-]+))?)[\s;]*Account Domain(:|=)""",
    """Account Domain(:|=)\s*({domain}[^:=]+?)[\s;]*Logon GUID(:|=)""",    
    """Service Name(:|=)\s*({dest_host}[^\s;]+\$)[\s;]*Service ID""",
    """Service Name(:|=)\s*({service_name}[^\s;]+)[\s;]*Service ID""",
    """Client Address(:|=)\s*(::[\w]+:)?({src_ip}[a-fA-F:\d.]+)""",
    """Failure Code(:|=)\s*({result_code}.+?)[\s;]*Transited Services(:|=)""",
    """Ticket Options(:|=)\s*({ticket_options}.+?)[\s;]*Ticket Encryption Type(:|=)"""
    """Ticket Encryption Type(:|=)\s*({ticket_encryption_type}.+?)[\s;]*Failure Code(:|=)"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```