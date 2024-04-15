#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-4769"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """<EventID>4769</EventID>"""
  """<Data Name ='ServiceName'>"""
  ]
  Fields = [
  """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({event_name}A Kerberos service ticket was requested)"""
  """<Computer>({host}[^<]+)</Computer>"""
  """<EventID>({event_code}[^<]+)</EventID>"""
  """<Data Name ='Status'>({result_code}[^<]+)</Data>"""
  """<Data Name ='ServiceName'>({dest_host}[\w-]+)\$</Data>"""
  """<Data Name ='ServiceName'>({service_name}[^<]+)</Data>"""
  """<Data Name ='TicketOptions'>({ticket_options}[^<]+)</Data>"""
  """<Data Name ='TicketEncryptionType'>({ticket_encryption_type}[^<]+)</Data>"""
  """<Data Name ='TargetUserName'>(([^\/<@]+\/+)({src_host}[^<@]+)(@({domain}[^<]+))?|(?=\w)({user}[^<@\s]+)(@({=domain}[^<@\s]+?))?)<\/Data>""",
  """<Data Name ='TargetDomainName'>(?=\w)({domain}[^<]+)</Data>"""
  """<Data Name ='IpAddress'>(::1|(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)</Data>"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]
  ParserVersion = "v1.0.0"


}
```