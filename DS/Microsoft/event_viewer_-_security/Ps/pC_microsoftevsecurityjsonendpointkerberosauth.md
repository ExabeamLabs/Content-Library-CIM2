#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-kerberosauth"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """McAfee_SIEM:"""
  """A Kerberos authentication ticket (TGT) was requested"""
]
Fields = [
  """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
  """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"id":\d*({event_code}4768)"""
  """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
  """"DomainID":"({domain}[^"]+)"""
  """"HostID":"({host}[^"]+)"""
  """"UserIDSrc":"({user}[\w\.\-]{1,40}\$?)"""
  """"CommandID":"({result_code}[^"]+)"""
  """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"Service_Name":"({service_name}[^"]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```