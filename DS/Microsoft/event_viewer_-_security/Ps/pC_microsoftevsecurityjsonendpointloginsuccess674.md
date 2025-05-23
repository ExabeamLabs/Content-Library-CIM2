#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-success-674
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy","MM/dd/yyyy hh:mm:ss a"]
  Conditions = [ "Service Ticket Renewed:", "Ticket Options:" ]
  Fields = [
    """({event_name}Account Logon)""",
    """({time}\d{2}\/\d{2}\/\d{4}\s+\d{2}:\d{2}:\d{2}\s+((?i)AM|PM))"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} \d{4})""",
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)\s*,\s*({host}[^,]+)""",
    """Computer(\w+)?["\s]*(:|=)\s*"?({host}.+?)("|\s)""",
    """({event_code}674)""",
    """User Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?).+?\s+""",
    """User Domain:\s*({domain}.+?)\s+Service Name:""",
    """Service Name:\s*({service_name}.+?)\s+Service ID:""",
    """Ticket Options:\s*({ticket_options}[^\s]+)""",
    """Ticket Encryption Type:\s*({ticket_encryption_type}[^\s]+)""",
    """Client Address:\s*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```