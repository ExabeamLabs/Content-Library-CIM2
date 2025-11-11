#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4769-6"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [
    """A Kerberos service ticket was requested"""
    """Account Name"""
    """":"Microsoft-Windows-Security-Auditing"""",
    """"EventID":4769,"""
  ]
  Fields = [
    """({event_name}A Kerberos service ticket was requested)"""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d(T|\s)\d\d:\d\d:\d\d)""",
    """\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s*[a-zA-Z]+"""
    """(::ffff:)?({host}[\w\-\.]+)\/Microsoft-Windows-Security-Auditing \(4769\)"""
    """"Computer(Name)?":"({host}[\w\-\.]+)"""
    """({event_code}4769)"""
    """Account Name(:|=)\s*(\\r|\\n|\\t)*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[\w._\-]+))?[\s;]*(\\r|\\n|\\t)*Account Domain(:|=)"""
    """Service Name(:|=)\s*(\\r|\\n|\\t)*(::ffff:)?({dest_host}[\w\-.]+\$)[\s;]*(\\r|\\n|\\t)*Service ID"""
    """Service Name(:|=)\s*(\\r|\\n|\\t)*({service_name}[^\s;]+?)[\s;]*(\\r|\\n|\\t)*Service ID"""
    """Client Address(:|=)\s*(::[\w]+:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-\.]+?))\s"""
    """Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}.+?))[\s;]*(\\r|\\n|\\t)*Transited Services(:|=)"""
    """Ticket Options(:|=)\s*(\\r|\\n|\\t)*({ticket_options}.+?)[\s;]*(\\r|\\n|\\t)*Ticket Encryption Type(:|=)"""
    """Ticket Encryption Type(:|=)\s*(\\r|\\n|\\t)*({ticket_encryption_type}.+?)(\\r|\\n\\t)*[\s;]*Failure Code(:|=)"""
    """Client Address(:|=)\s*(\\r|\\n|\\t)*(::[\w]+:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))"""
    """Client Port:(\\n|\\r|\\t)*({src_port}\d+)"""
    """Computer(Name)?=({host}[\w\-\.]+)([^\s]*\s|;)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  ]
  ParserVersion = "v1.0.0"


}
```