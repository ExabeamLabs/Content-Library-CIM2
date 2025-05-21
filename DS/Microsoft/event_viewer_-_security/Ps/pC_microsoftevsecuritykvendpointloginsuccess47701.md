#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-4770-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy","MM/dd/yyyy hh:mm:ss a"]
  Conditions = [ """MSWinEventLog""", """4770 Microsoft-Windows-Security-Auditing""", """A Kerberos service ticket was renewed""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))""",
    """({event_name}A Kerberos service ticket was renewed)""",
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})""",
    """({event_code}4770)""",
    """(Information|Audit Success|Success Audit)\s+({host}[\w.\-]+)\s+""",
    """Microsoft-Windows-Security-Auditing\s+(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Account Name:\s+(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}.+?))?\s+Account Domain:""",
    """Account Domain:\s+(?=\w)({domain}.+?)\s+Service Information:""",
    """Client Address:\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+Client Port""",
    """Service Name:\s+(?=\w)({service_name}.+?)\s+Service ID:""",
    """Service Name:\s+(?=\w)({dest_host}[\w\-.]+?\$)\s+Service ID:""",
    """Ticket Options:\s+({ticket_options}.+?)\s+Ticket Encryption Type:""",
    """Ticket Encryption Type:\s+({ticket_encryption_type}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```