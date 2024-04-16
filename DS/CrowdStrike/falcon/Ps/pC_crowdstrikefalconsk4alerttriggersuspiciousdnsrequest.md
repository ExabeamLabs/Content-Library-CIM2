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
     """"DomainName":"({domain}[^"]+)""",
     """"event_simpleName":"({event_code}[^"]+)""",
     """"event_platform":"({os}[^"]+)"""",
     """"aid":"({aid}[^"]+)""",
     """"DomainName":"([^"]+\.)?({top_domain}[^\."]+\.[^\."]+)"""",
     """"cid":"({cid}[^"]+)""",
     """"OciContainerId"\s*:\s*"({container_id}[^"]+)"""",
     """exa_json_path=$.aip,exa_field_name=host""",
		 """exa_json_path=$.timestamp,exa_field_name=time""",
		 """exa_json_path=$.DomainName,exa_field_name=domain""",
	   """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
		 """exa_json_path=$.event_platform,exa_field_name=os""",
		 """exa_json_path=$.aid,exa_field_name=aid""",
		 """exa_json_path=$.DomainName,exa_regex=([^"]+\.)?({top_domain}[^\."]+\.[^\."]+)""",
		 """exa_json_path=$.cid,exa_field_name=cid"""
     """exa_json_path=$.OciContainerId,exa_field_name=container_id"""
    ]
    DupFields = ["event_code->alert_name", "event_code->alert_type", "event_code->alert_subject", "domain->web_domain"]


}
```