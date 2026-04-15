#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-activity-idpentityriskscorechange"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = "epoch"
Conditions = [
  """"event_simpleName":"IdpEntityRiskScoreChange""""
  """"vendor":"CrowdStrike""""
  """"event_platform":""""
]
Fields = [
  """exa_json_path=$.timestamp,exa_field_name=time""",
  """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
  """exa_json_path=$.aid,exa_field_name=aid""",
  """exa_json_path=$.cid,exa_field_name=cid""",
  """exa_json_path=$.name,exa_field_name=event_name""",
  """exa_json_path=$.event_category,exa_field_name=event_category"""
  """exa_json_path=$.host,exa_regex=({host}[\w\-\.]+)"""
  """exa_json_path=$.DnsHostName,exa_field_name=src_host"""
]
ParserVersion = "v1.0.0"


}
```