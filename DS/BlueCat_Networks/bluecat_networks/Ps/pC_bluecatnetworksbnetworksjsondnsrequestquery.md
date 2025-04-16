#### Parser Content
```Java
{
Name = bluecatnetworks-bnetworks-json-dns-request-query
  Vendor = BlueCat Networks
  Product = BlueCat Networks
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ """"query":""", """"queryType":""", """"extracted_source":""", """"matchedPolicies":""", """"actionTaken":""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.actionTaken,exa_field_name=action""",
    """exa_json_path=$.query,exa_field_name=dns_query""",
    """exa_json_path=$.queryType,exa_field_name=dns_query_type""",
    """exa_json_path=$.site,exa_field_name=site_at""",
    """exa_json_path=$.response,exa_field_name=dns_response_code""",
    """exa_json_path=$.matchedPolicies[0].id,exa_field_name=policy_id""",
    """exa_json_path=$.matchedPolicies[0].name,exa_field_name=policy_name""",
    """exa_json_path=$.extracted_source,exa_field_name=src_ip"""
  ]
  ParserVersion = "v1.0.0"


}
```