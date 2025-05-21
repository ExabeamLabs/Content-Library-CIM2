#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-endpoint-login-4769"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [
    """<EventID>4769</EventID>"""
    """A Kerberos service ticket was requested"""
    """Account Name"""
    """Microsoft-Windows-Security-Auditing"""
  ]
  Fields = [
    """({event_name}A Kerberos service ticket was requested)"""
    """TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\d\d\dZ)'\/>"""
    """Computer>({host}[\w\-.]+)<\/Computer"""
    """({event_code}4769)"""
    """Account Name(:|=)\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[\w._\-]+))?[\s;]*Account Domain(:|=)"""
    """Service Name(:|=)\s*({src_host}[\w\-.]+\$)[\s;]*Service ID"""
    """Service Name(:|=)\s*({service_name}[^\s;]+)[\s;]*Service ID"""
    """Client Address(:|=)\s*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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