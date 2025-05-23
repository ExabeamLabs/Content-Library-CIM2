#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4768-6"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
  """LogType="WLS""""
  """EventID="4768""""
]
Fields = [
  """({time}\w+ \d+ \d+:\d+:\d+( \d\d\d\d)?)"""
  """Computer="+({host}[^"]+)""""
  """"({time}\d\d\d\d\-\d+\-\d+T\d\d:\d\d:\d\d)"""
  """EventID="+({event_code}[^"]+)""""
  """EventRecordID="+({event_id}[^"]+)""""
  """TargetUserName ="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """TargetDomainName ="+({domain}[^"]+)""""
  """TargetSid="+({user_sid}[^"]+)""""
  """IpAddress="+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Status="+({result_code}[^"]+)""""
  """ServiceName ="({service_name}[^"]+)"""
  """TicketEncryptionType="({ticket_encryption_type}[^"]+)"""
  """TicketOptions="({ticket_options}[^"]+)"""
]
DupFields = [ "user_sid->dest_user_sid" , "domain->dest_domain", "user->dest_user" ]
ParserVersion = "v1.0.0"


}
```