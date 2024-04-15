#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-4776"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """<EventID>4776</EventID>"""
  """'Status'>"""
  ]
  Fields = [
  """SystemTime(\\)?=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
  """<Data Name(\\)?='Workstation'>(\\+)?(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(?:(?!NULL)(\\*({src_host}[^<"]+))))<\/Data>"""
  """<Computer>({host}[^<]+)</Computer>"""
  """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials"""
  """<EventID>({event_code}\d+)</EventID>"""
  """<Computer>(?!(?:[A-Fa-f:\d.]+))[^<.]+(\.({domain}[^<]+)[^<]*)?</Computer>""",
  """<Data Name(\\)?='TargetUserName'>(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+))(?<!local)(?<!loc)|(({domain}[^<\\]+)\\+)?(null|({user}[^<;@]+))|({=user}[^@<;]+?)(?:@({=domain}[^<.]+)[^<]*)?)<\/Data>"""
  """<Data Name(\\)?='Status'>({result_code}[^<]+)</Data>"""
  """<Keywords><Keyword>({result}[^<]+)<""",
  """Workstation:\s*({src_host}[^"\s]+)"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = ["host->dest_host"]


}
```