#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-4776"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [
  """<EventID>4776</EventID>""",
  """Status""",
  """TargetUserName""",
  """<Data Name""",
  """</Data>"""
  ]
  Fields = [
  """SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)"""
  """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
  """<Data Name(\\)?=('|")Workstation('|")>(\\+)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(?:(?!NULL)((?i)(workstation)|(\\*({src_host}[\w\-.]+)))))<\/Data>""",
  """<Computer>(\w+\.({domain}[^<]+))"""
  """<Computer>({host}[\w\-.]+)</Computer>"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials"""
  """<EventID>({event_code}\d+)</EventID>"""
  """<Computer>(?!(?:[A-Fa-f:\d.]+))[^<.]+(\.({domain}[^<]+)[^<]*)?</Computer>""",
  """<Data Name(\\)?=('|")TargetUserName('|")>\s*(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?<!local)(?<!loc)|(({domain}[^<\\]+)\\+)?(null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(?:@({=domain}[^<.]+)[^<]*)?)<\/Data>"""
  """<Data Name(\\)?=('|")Status('|")>((?-i)\\+[rnt])*\s*({result_code}[^<]+)<\/Data>"""
  """<Keywords><Keyword>({result}[^<]+)<""",
  """Source Workstation(:|=)[\s\\\t]*((({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+))(:({src_port}\d+))?)|((?i)(workstation)|({src_host}[\w\-.]+?)))[\s\\\\n\;]*Error Code(:|=)"""
  """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [
    "result_code->failure_code"
    "result_code->error_code"
    ]
  ParserVersion = "v1.0.0"


}
```