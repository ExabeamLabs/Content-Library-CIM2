#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4769"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """4769"""
    """"TransmittedServices":""""
  ]
  Fields = [
    """({event_name}A Kerberos service ticket was requested)"""
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"EventReceivedTime":\s*({time}\d+)"""
    """"timestamp":\s*({time}\d+)"""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
    """"+created"+:"+({time}[^"]+)"""
    """"TimeCreated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"Computer"+:"+({host}[^"]+)""""
    """"+(?:winlog\.)?computer_name"+:"+({host}[^"]+)"""
    """"(Hostname|MachineName)":"({host}[^"]*)"""
    """({event_code}4769)"""
    """"TargetUserName":"({user}[^@"]+)"""
    """"TargetDomainName":"({domain}[^."]+)"""
    """"ServiceName":"({dest_host}[^@"]+\$)""""
    """"ServiceName":"({service_name}[^@"]+)""""
    """"TicketOptions":"({ticket_options}[^"]+)"""
    """"TicketEncryptionType":"({ticket_encryption_type}[^"]+)"""
    """"IpAddress":"(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"Status":"({result_code}[^"]+)"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```