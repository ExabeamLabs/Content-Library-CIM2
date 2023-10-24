#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4768-6"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """LogType="WLS""""
  """EventID="4768""""
]
Fields = [
  """Computer="+({host}[^"]+)""""
  """"({time}\d\d\d\d\-\d+\-\d+T\d\d:\d\d:\d\d)"""
  """EventID="+({event_code}[^"]+)""""
  """EventRecordID="+({event_id}[^"]+)""""
  """TargetUserName ="+({user}[\w\.\-]{1,40}\$?)""""
  """TargetDomainName ="+({domain}[^"]+)""""
  """TargetSid="+({user_sid}[^"]+)""""
  """IpAddress="+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Status="+({result_code}[^"]+)""""
  """ServiceName ="({service_name}[^"]+)"""
  """TicketEncryptionType="({ticket_encryption_type}[^"]+)"""
  """TicketOptions="({ticket_options}[^"]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```