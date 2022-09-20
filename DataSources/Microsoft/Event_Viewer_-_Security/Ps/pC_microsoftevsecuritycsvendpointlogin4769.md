#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-endpoint-login-4769
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Kerberos Service Ticket Operations""", """Microsoft-Windows-Security-Auditing""","""TicketEncryptionType:""", """TicketOptions:""", """4769""", """TransmittedServices:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}[+\-]+\d\d:\d\d""",
    """({host}[^\s]+)\s+Kerberos Service Ticket Operations""",
    """({event_code}4769)""",
    """TargetUserName:({user}[^@]+)@({domain}[^,]+),""",
    """TargetDomainName:({domain}[^,]+),""",
    """ServiceName:({dest_host}[^,\s\\]+)""",
    """TicketOptions:({ticket_options}[^,]+),""",
    """TicketEncryptionType:({ticket_encryption_type}[^,]+),""",
    """Status:({result_code}[^,]+),""",
    """IpAddress:(::ffff:)?({src_ip}[a-fA-F\d:.]+),""",
    """({action}(Success|Failure) Audit)"""
  ]


}
```