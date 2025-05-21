#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4769-2"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy", "epoch_sec","MM/dd/yyyy HH:mm:ss a"]
  Conditions = [
    """A Kerberos service ticket was requested"""
    """Account Name"""
    """Microsoft-Windows-Security-Auditing""",
    """4769 """
  ]
  Fields = [
    """({event_name}A Kerberos service ticket was requested)"""
    """(?i)({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|pm))"""
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """TimeGenerated=({time}\d{10})"""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s*[a-zA-Z]+"""
    """(::ffff:)?({host}[\w\-\.]+)\/Microsoft-Windows-Security-Auditing \(4769\)"""
    """"ComputerName":"({host}[\w\-\.]+)"""
    """({event_code}4769)"""
    """Account Name(:|=)\s*((?-i)\\+[rnt])*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[\w._\-]+))?[\s;]*((?-i)\\+[rnt])*Account Domain(:|=)"""
    """Service Name(:|=)\s*((?-i)\\+[rnt])*(::ffff:)?({dest_host}[\w\-.]+\$)[\s;]*((?-i)\\+[rnt])*Service ID"""
    """Service Name(:|=)\s*((?-i)\\+[rnt])*({service_name}[^\s;]+?)[\s;]*((?-i)\\+[rnt])*Service ID"""
    """Client Address(:|=)\s*(::[\w]+:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-\.]+?))\s"""
    """Failure Code(:|=)\s*((?-i)\\+[rnt])*({result_code}[^\s]+)[\s;]*((?-i)\\+[rnt])*.+?Transited Services(:|=)"""
    """Ticket Options(:|=)\s*((?-i)\\+[rnt])*({ticket_options}[^\s]+)[\s;]*((?-i)\\+[rnt])*.+?Ticket Encryption Type(:|=)"""
    """Ticket Encryption Type(:|=)\s*((?-i)\\+[rnt])*({ticket_encryption_type}.+?)(\\r|\\n\\t)*[\s;]*Failure Code(:|=)"""
    """Client Address(:|=)\s*((?-i)\\+[rnt])*(::[\w]+:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))"""
    """Client Port:(\\n|\\r|\\t)*({src_port}\d+)"""
    """\sComputer(Name)?=({host}[\w\-\.]+)([^\s]*\s|;)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """Microsoft-Windows-Security-Auditing.+?Success Audit ({host}[\w\-\.]+)"""
    """Error Code:(\\t|\\r\\n)*({result_code}[\w\-]+)\s*(\\t|\\r|\\n)*"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]
  ParserVersion = "v1.0.0"


}
```