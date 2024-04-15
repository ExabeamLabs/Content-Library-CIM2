#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4768"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """:4768"""
    """"ServiceName":""""
    """Pre-Authentication"""
  ]
  Fields = [
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"EventReceivedTime":\s*({time}\d+)"""
    """"timestamp":\s*({time}\d+)"""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)""""
    """"(Hostname|MachineName|(?:winlog\.)?computer_name)":"({host}[^"]*)"""
    """({event_code}4768)"""
    """"(TargetUserName|AccountName)":"({user}[^"]+)"""
    """"(TargetDomainName|SuppliedRealmName)":"({domain}[^."]+)"""
    """"(UserID|TargetSid)":"({user_sid}[^"]+)"""
    """"(IpAddress|ClientAddress)":"(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"(Status|ResultCode)":"({result_code}[^"]+)"""
    """"TicketOptions":"({ticket_options}[^"]+)"""
    """"TicketEncryptionType":"({ticket_encryption_type}[^"]+)"""
    """"ServiceName":"({service_name}[^"]+)"""
  ]


}
```