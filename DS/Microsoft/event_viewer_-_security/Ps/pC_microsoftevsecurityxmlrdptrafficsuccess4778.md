#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-rdp-traffic-success-4778"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """<EventID>4778<"""
  ]
  Fields = [
  """<TimeCreated SystemTime(\\)?='({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
  """<Computer>({host}[\w\-.]+)"""
  """({event_name}A session was reconnected to a Window Station)"""
  """({event_code}4778)"""
  """<EventRecordID>({event_id}[^<]+)"""
  """'AccountName'>({user}[^"\s<]+)<"""
  """'AccountDomain'>({domain}[^"\s<]+)<"""
  """'LogonID'>({login_id}[^"\s<]+)<"""
  """'ClientName'>({src_host}[\w\-.]+)<"""
  """'ClientAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<"""
  ]
  ParserVersion = "v1.0.0"


}
```