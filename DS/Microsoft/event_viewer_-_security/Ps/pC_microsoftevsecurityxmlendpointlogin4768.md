#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-4768"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """<EventID>4768</EventID>"""
  """<Data Name"""
  """TargetSid"""
  ]
  Fields = [
  """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
  """<Computer>({host}[\w.-]+)</Computer>"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<EventID>({event_code}\d+)</EventID>"""
  """<Data Name\\*=('|")TargetSid('|")>(NULL SID|({user_sid}[^<]+))</Data>"""
  """<Data Name\\*=('|")Status('|")>({result_code}[^<]+)</Data>"""
  """Account Name(:|=)\s*(\\t|\\r|\\n)*({user}[\w\.\-]{1,40}\$?)(?:@.+?)?[\s;]*(\\t|\\r|\\n)*"?\s*Supplied Realm Name"""
  """<Data Name\\*=('|")TargetUserName('|")>\s*(?=\w)([^"'<]+?('|"))?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|<]+\.[^\]\s<"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)\s*(@({domain}[^@<=]+))?)"?<\/Data>""",
  """<Data Name\\*=('|")TargetDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
  """<Data Name\\*=('|")IpAddress('|")>(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>"""
  """<Data Name\\*=('|")TicketEncryptionType('|")>({ticket_encryption_type}[^<]+)</Data>"""
  """<Data Name\\*=('|")TicketOptions('|")>({ticket_options}[^<]+)</Data>"""
  """<Data Name\\*=('|")ServiceName('|")>({service_name}[^\/\\<]+)""",
  """<Data Name\\*=('|")PreAuthType('|")>({auth_type}[^<]+)<""",
  """<Opcode>(0|({opcode}[^<]+))""",
  """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```