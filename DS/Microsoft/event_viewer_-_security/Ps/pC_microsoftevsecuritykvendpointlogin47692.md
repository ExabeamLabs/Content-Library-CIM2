#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4769-2"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """A Kerberos service ticket was requested"""
    """Account Name"""
    """Microsoft-Windows-Security-Auditing"""
  ]
  Fields = [
    """({event_name}A Kerberos service ticket was requested)"""
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))"""
    """(::ffff:)?({host}[^\s\/]+)\/Microsoft-Windows-Security-Auditing \(4769\)"""
    """({event_code}4769)"""
    """Account Name(:|=)\s*({user}[^@:\s;]+)(@({domain}[\w._\-]+))?[\s;]*Account Domain(:|=)"""
    """Service Name(:|=)\s*(::ffff:)?({dest_host}[^\s;]+\$)[\s;]*Service ID"""
    """Service Name(:|=)\s*({service_name}[^\s;]+)[\s;]*Service ID"""
    """Client Address(:|=)\s*(::[\w]+:)?(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-\.]+?))\s"""
    """Failure Code(:|=)\s*({result_code}.+?)[\s;]*Transited Services(:|=)"""
    """Ticket Options(:|=)\s*({ticket_options}.+?)[\s;]*Ticket Encryption Type(:|=)"""
    """Ticket Encryption Type(:|=)\s*({ticket_encryption_type}.+?)[\s;]*Failure Code(:|=)"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]
  ParserVersion = "v1.0.0"


}
```