#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-service-create-success-4697-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
  """EventID=4697"""
  """Service File Name:"""
]
Fields = [
  """\WComputer=({dest_host}({host}[\w\.\-]+))"""
  """\WEventID=({event_code}\d+)"""
  """\WTimeGenerated=({time}\d{10})"""
  """\WSecurity ID:\s*(|({user_sid}.+?))\s+Account Name:"""
  """\WAccount Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\WAccount Domain:\s*({domain}[^\s]+)"""
  """\WLogon ID:\s*({login_id}[^\s]+)"""
  """Service Name:\s*(\\+r|\\+t|\\+n)*(({service_name}[^=:\\_]+?)(_[^"\<]+?)?)\s*(\\+r|\\+t|\\+n)*Service """
  """\WService File Name:\s*(|({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?)))\s+Service Type:"""
  """\WService Type:\s*(|({service_type}.+?))\s+Service Start Type:"""
  """\WService Account:\s*(({account_domain}[^\\]+)\\)?({account_name}.+?)\s*$"""
]
ParserVersion = "v1.0.0"


}
```