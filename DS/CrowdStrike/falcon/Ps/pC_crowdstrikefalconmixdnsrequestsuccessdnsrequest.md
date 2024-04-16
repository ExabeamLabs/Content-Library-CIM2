#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-dns-request-success-dnsrequest"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
ExtractionType = json
Conditions = [
""""event_simpleName":"""
""""DnsRequest""""
""""RequestType":"""
]
Fields = [
  """"OciContainerId"\s*:\s*"({container_id}[^"]+)"""",
  """"hostname":"({host}[\w\-.]+)"""",
  """"timestamp":\s*"({time}\d{10})""",
  """"DomainName":\s*"({query}[^\"]+?)\s*"""",
  """"aip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"LocalAddressIP6":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"RemoteAddressIP6":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"LocalAddressIP4":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"RemoteAddressIP4":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"LocalPort":\s*"({src_port}\d+)""",
  """"RemotePort":\s*"({dest_port}\d+)""",
  """"aid":\s*"({aid}[^\"]+)"""",
  """"aip":\s*"({aip}[a-fA-F:\d.]+)""",
  """"event_simpleName":\s*"({event_code}[^\"]+)"""",
  """"event_platform":"({os}[^"]+)"""",
  """src-account-name":"({account_name}[^"]+)""",
  """"IP4Records":"({dns_response}[^"]+)"""",
  """"ContextProcessId":"({process_guid}[^"]+)"""",
  """"FirstIP4Record":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
  """"QueryStatus":"({dns_query_flags}[^"]+)"""",
  """"RequestType":"({dns_query_type}[^"]+)""""
  """exa_json_path=$.OciContainerId,exa_field_name=container_id"""
  """exa_json_path=$.hostname,exa_regex=({host}[\w\-.]+)"""
  """exa_json_path=$.timestamp,exa_field_name=time"""
  """exa_json_path=$.DomainName,exa_regex=({query}[^\"]+?)\s*"""
  """exa_regex="DomainName":\s*"({query}[^\"]+?)\s*"""",
  """exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.LocalAddressIP6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.RemoteAddressIP6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.RemoteAddressIP4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_json_path=$.LocalPort,exa_field_name=src_port"""
  """exa_json_path=$.RemotePort,exa_field_name=dest_port"""
  """exa_json_path=$.aid,exa_field_name=aid"""
  """exa_json_path=$.aip,exa_regex=({aip}[a-fA-F:\d.]+)""",
  """exa_json_path=$.event_simpleName,exa_field_name=event_code"""
  """exa_json_path=$.event_platform,exa_field_name=os"""
  """exa_json_path=$.src-account-name,exa_field_name=account_name"""
  """exa_json_path=$.IP4Records,exa_field_name=dns_response"""
  """exa_json_path=$.ContextProcessId,exa_field_name=process_guid"""
  """exa_json_path=$.FirstIP4Record,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
  """exa_json_path=$.QueryStatus,exa_field_name=dns_query_flags"""
  """exa_json_path=$.RequestType,exa_field_name=dns_query_type"""
]
ParserVersion = "v1.0.0"


}
```