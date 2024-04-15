#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-dns-request-success-dnsrequest"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"""
""""DnsRequest""""
""""RequestType":"""
]
Fields = [
  """"hostname":"({host}[\w\-.]+)"""",
  """"timestamp":\s*"({time}\d{10})"""",
  """"DomainName":\s*"({query}[^\"]+)"""",
  """"aip":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"LocalAddressIP6":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"RemoteAddressIP6":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"LocalAddressIP4":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"RemoteAddressIP4":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"LocalPort":\s*"({src_port}\d+)""",
  """"RemotePort":\s*"({dest_port}\d+)""",
  """"aid":\s*"({aid}[^\"]+)"""",
  """"aip":\s*"({aip}[a-fA-F:\d.]+)""",
  """"event_simpleName":\s*"({event_code}[^\"]+)"""",
  """src-account-name":"({account_name}[^"]+)""",
  """"IP4Records":"({dns_response}[^"]+)"""",
  """"ContextProcessId":"({process_guid}[^"]+)"""",
  """"FirstIP4Record":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
]
ParserVersion = "v1.0.0"


}
```