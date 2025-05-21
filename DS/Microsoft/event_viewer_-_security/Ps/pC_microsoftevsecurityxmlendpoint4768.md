#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-4768"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """"EventID":"4768""""
  """<Data Name"""
]
Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"Computer":"({host}[^"]+)"""
  """"EventID":"({event_code}\d+)"""
  """<Data Name\\*=('|")TargetSid('|")>({user_sid}[^<]+)</Data>"""
  """<Data Name\\*=('|")Status('|")>({result_code}[^<]+)</Data>"""
  """<Data Name\\*=('|")TargetUserName('|")>(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>"""
  """<Data Name\\*=('|")TargetDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
  """<Data Name\\*=('|")IpAddress('|")>(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """<Data Name\\*=('|")TicketEncryptionType('|")>({ticket_encryption_type}[^<]+)</Data>"""
  """<Data Name\\*=('|")TicketOptions('|")>({ticket_options}[^<]+)</Data>"""
  """<Data Name\\*=('|")ServiceName('|")>({service_name}[^<]+)</Data>"""
  """"Activity":"({event_name}[^"]+)"""
  """<Level>({run_level}[^<]+)<"""
]
DupFields = [ "domain->dest_domain", "user->dest_user" ]
ParserVersion = "v1.0.0"


}
```