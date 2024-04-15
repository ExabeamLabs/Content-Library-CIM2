#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-authfailed"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """McAfee_SIEM:"""
  """Kerberos pre-authentication failed"""
]
Fields = [
  """({event_name}Kerberos pre-authentication failed)"""
  """"src_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """id":\d*({event_code}4771)"""
  """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
  """"DomainID":"({domain}[^"]+)"""
  """"HostID":"({host}[^"]+)"""
  """"UserIDSrc":"({user}[^"]+)"""
  """"Security_ID":"({user_sid}[^"]+)"""
  """"Service_Name":"({service_name}[^"]+)"""
  """"CommandID":"({result_code}[^"]+)"""
]
DupFields = [
  "host->dest_host"
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```