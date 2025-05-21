#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-success-4770-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss" ]
  Conditions = [ """"EventID":4770""", """"Category":"Kerberos Service Ticket Operations"""", """"SourceName":"Microsoft-Windows-Security-Auditing"""", """"TargetUserName":"""" ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s+\d\d:\d\d:\d\d)""",
    """"Hostname":"({host}[\w\-.]+)"""",
    """({event_name}(A Kerberos service ticket was renewed|Kerberos Service Ticket Operations))""",
    """"EventID":({event_code}[\w\-.]+),""",
    """"TargetUserName":"(({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@[^"]+?)?""""
    """"TargetDomainName":"({domain}[^"]+)""""
    """"ServiceName":"({service_name}[^"]+)""""
    """"TicketOptions":"({ticket_options}[^"]+)""""
    """"TicketEncryptionType":"({ticket_encryption_type}[^"]+)""""
    """"IpAddress":"(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"IpPort":"({src_port}\d+)""",
    """"ServiceName":"({dest_host}[\w\-.]+\$)""""
  ]
  ParserVersion = "v1.0.0"


}
```