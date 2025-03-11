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
    """TargetUserName:({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^,]+),""",
    """TargetDomainName:({domain}[^,]+),""",
    """ServiceName:({src_host}[\w\-.]+\$)""",
    """TicketOptions:({ticket_options}[^,]+),""",
    """TicketEncryptionType:({ticket_encryption_type}[^,]+),""",
    """Status:({result_code}[^,]+),""",
    """IpAddress:(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """({result}(Success|Failure) Audit)"""
  ]
  DupFields = [ "domain->dest_domain", "user->dest_user" ]


}
```