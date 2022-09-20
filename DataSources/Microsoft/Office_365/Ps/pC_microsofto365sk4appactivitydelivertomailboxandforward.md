#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-delivertomailboxandforward
  Vendor = Microsoft
  Product = Office 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""Operation":"Set-Mailbox""" , """DeliverToMailboxAndForward""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """Forward.+?Value":"(smtp:)?({target}[^"]+@({dest_domain}[^"]+))""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"\[?({src_ip}((\d{1,3}\.){1,3}\d{1,3}|[a-fA-F\d]+:[A-Fa-f\d:]+))\]?(:({src_port}\d+))?"""",
    """({operation}DeliverToMailboxAndForward)"""",
    """msg=({additional_info}.+?)\srequest=""",
    """"Value":"(smtp:)?.+?@({dest_domain}[^"]+)"""",
    """UserId":"({email_address}[^"\\\s@]+@({domain}[^"\\\s@]+))""",
    """({app}Office 365)"""
    """destinationServiceName =({app}.+?)\sdevice"""
  ]
  DupFields = ["domain->email_domain"]


}
```