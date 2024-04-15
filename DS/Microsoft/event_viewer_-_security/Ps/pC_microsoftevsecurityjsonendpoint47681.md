#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-4768-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """A Kerberos authentication ticket (TGT) was requested"""
  """"event_id":"4768""""
  """"account_information-SuppliedRealmName":""""
]
Fields = [
  """"time":"({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))""""
  """"host":"({host}[^"]+)\s*"""
  """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
  """({event_code}4768)"""
  """"account_information-AccountName":"\s*({user}[^"@]+)\s*"""
  """"network_information-ClientAddress":"\s*(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """"additional_information-ResultCode":"\s*({result_code}[^"]+)\s*""""
  """"account_information-SuppliedRealmName":"\s*({domain}[^"]+)\s*""""
  """"account_information-UserID":"\s*(?:NULL SID|({user_sid}[^"]+))\s*""""
  """"service_information-ServiceName":"({service_name}[^"]+)"""
  """"additional_information-TicketEncryptionType":"({ticket_encryption_type}[^"]+)"""
  """"additional_information-TicketOptions":"({ticket_options}[^"]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```