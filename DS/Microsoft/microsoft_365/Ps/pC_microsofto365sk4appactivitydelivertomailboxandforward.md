#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-delivertomailboxandforward
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""Operation":"Set-Mailbox""" , """DeliverToMailboxAndForward""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """Forward.+?Value":"(smtp:)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"\[?({src_ip}((\d{1,3}\.){1,3}\d{1,3}|[a-fA-F\d]+:[A-Fa-f\d:]+))\]?(:({src_port}\d+))?"""",
    """({operation}DeliverToMailboxAndForward)"""",
    """msg=({additional_info}.+?)\srequest=""",
    """"Value":"(smtp:)?[^@"]+@({dest_email_domain}[^"]+?)"""",
    """UserId":"({email_address}[^"\\\s@]+@({email_domain}[^"\\\s@]+\.[^"\\\s@]+))""",
    """({app}Office 365)"""
    """destinationServiceName =({app}.+?)\sdevice"""
    """"CorrelationId":\s*"({correlation_id}[^"]+)""""
  ]


}
```