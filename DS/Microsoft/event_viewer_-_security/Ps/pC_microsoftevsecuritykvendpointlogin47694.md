#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-4769-4
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = ["""A Kerberos service ticket was requested""", """Account Name""", """Computer"""]
  Fields = [
    """({event_name}A Kerberos service ticket was requested)""",
    """({time}\d\d\d\d-\d\d-\d\d(\s|T)\d\d:\d\d:\d\d)"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
    """<Computer>({host}[^<]+)</Computer>""",
    """Computer(\w+)?["\s]*(:|=)\s*"?({host}.+?)("|\s|;)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_code}4769)""",
    """Account Name(:|=)(\s|\\[rnt])*(\w+\/({src_host}[^@\s]+)(@({domain}[\w._\-]+))?|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[\w._\-]+))?)[\s;]*(\s|\\[rnt]|;)*Account Domain(:|=)""",
    """Account Domain(:|=)(\s|\\[rnt])*(|({domain}[^\\:=]+?))(\s|\\[rnt]|;)*Logon GUID(:|=)"""
    """Service Name(:|=)(\s|\\[rnt])*({dest_host}[\w\-.]+)\$(\s|\\[rnt]|;)*Service ID""",
    """Service Name(:|=)(\s|\\[rnt])*({service_name}[^\\\s;]+)(\s|\\[rnt]|;)*Service ID""",
    """Client Address(:|=)\s*(\\[rnt])*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Failure Code(:|=)(\s|\\[rnt])*({result_code}[^\s]+)(\s|\\[rnt]|;)*.+?Transited Services(:|=)"""
    """Ticket Options(:|=)(\s|\\[rnt])*({ticket_options}[^\s]+)(\s|\\[nrt]|;)*.+?Ticket Encryption Type(:|=)"""
    """Ticket Encryption Type(:|=)(\s|\\[rnt])*({ticket_encryption_type}[^\s]+)(\s|\\[nrt]|;)*.+?Failure Code(:|=)"""
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```