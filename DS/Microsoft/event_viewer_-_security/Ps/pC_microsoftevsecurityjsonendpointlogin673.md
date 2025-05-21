#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-673
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat ="MMM dd HH:mm:ss yyyy"
  Conditions = [ "Service Ticket Request:", "Ticket Options:" ]
  Fields = [
    """({event_name}Account Logon)""",
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
    """({event_code}673)""",
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)\s*,\s*({host}[^,]+)""",
    """Security(,|\srn=|\s+)({event_id}\d+)""",
    """User Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """User Domain:\s*({domain}[^\s]+)\s""",
    """Client Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Service Name:\s*({dest_host}\S+\$)\s""",
    """Service Name:\s*({service_name}\S+)""",
    """Failure Code:\s*({result_code}[\w\-]+)""",
    """Ticket Options:\s*({ticket_options}[^\s]+)""",
    """Ticket Encryption Type:\s*({ticket_encryption_type}[^\s]+)"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```