#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-4768"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """CEF:"""
  """"eventID":"4768""""
  """A Kerberos authentication ticket (TGT) was requested"""
]
Fields = [
  """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
  """"computer":"({host}[\w\-.]+)"""
  """"message":"({event_name}[^"]+?)\s*""""
  """"eventID":"({event_code}\d+)"""
  """"eventRecordID":"({event_id}\d+)"""
  """"severityValue":"({result}[^"]+?)\s*""""
  """"targetSid":"({dest_user_sid}({user_sid}[^"\s]+?))\s*""""
  """"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*""""
  """"targetDomainName":"({dest_domain}({domain}[^"\s]+?))\s*""""
  """"status":"({failure_code}({result_code}[^"]+?))\s*""""
  """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"ticketEncryptionType":"({ticket_encryption_type}[^"]+)"""
  """ticketOptions":"({ticket_options}[^"]+)"""
  """"serviceName":"({service_name}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```