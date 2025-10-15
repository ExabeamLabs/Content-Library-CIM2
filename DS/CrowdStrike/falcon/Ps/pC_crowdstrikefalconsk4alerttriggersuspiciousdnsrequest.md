#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-alert-trigger-suspiciousdnsrequest
   Vendor = CrowdStrike
   ParserVersion = "v1.0.0"
   Product = Falcon
   ExtractionType = json
   TimeFormat = ["epoch_sec","epoch"]
   Conditions = [ """"event_simpleName":"SuspiciousDnsRequest"""" ]
   Fields = [
     """"aip":"({host}[^"]+)"""
     """"timestamp":"({time}\d{10})""",
     """"DomainName":"({dns_query}({web_domain}[^"]+))""",
     """"event_simpleName":"({alert_subject}({alert_type}({alert_name}({event_code}[^"]+))))""",
     """"event_platform":"({os}[^"]+)"""",
     """"aid":"({aid}[^"]+)""",
     """"cid":"({cid}[^"]+)""",
     """"OciContainerId"\s*:\s*"({container_id}[^"]+)"""",
     """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"ComputerName":"({host}[\w\-\.]+)"""",
     """"aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """exa_json_path=$.aip,exa_field_name=host""",
     """exa_json_path=$.timestamp,exa_field_name=time""",
     """exa_json_path=$.DomainName,exa_field_name=web_domain""",
     """exa_json_path=$.DomainName,exa_field_name=dns_query""",
     """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
     """exa_json_path=$.event_simpleName,exa_field_name=alert_name""",
     """exa_json_path=$.event_simpleName,exa_field_name=alert_type""",
     """exa_json_path=$.event_simpleName,exa_field_name=alert_subject""",
     """exa_json_path=$.event_platform,exa_field_name=os""",
     """exa_json_path=$.aid,exa_field_name=aid""",
     """exa_json_path=$.cid,exa_field_name=cid""",
     """exa_json_path=$.OciContainerId,exa_field_name=container_id""",
     """exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)""",
     """exa_json_path=$.aip,exa_field_name=aip"""
    ]


}
```