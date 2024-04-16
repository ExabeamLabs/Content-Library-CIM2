#### Parser Content
```Java
{
Name = "cisco-cloudlock-json-alert-trigger-success-entityowneremail"
Vendor = "Cisco"
Product = "Cisco CloudLock"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSz"
Conditions = [
""""entity_vendor_name":"""
""""entity_owner_email":"""
""""ctx_after":"""
]
Fields = [
"""exa_json_path=$.created_at,exa_field_name=time""",
"""exa_json_path=$.id,exa_field_name=alert_id""",
"""exa_json_path=$.policy_name,exa_field_name=alert_name""",
"""exa_json_path=$.entity_origin_type,exa_field_name=alert_type""",
"""exa_json_path=$.severity,exa_field_name=alert_severity""",
"""exa_json_path=$.entity_name,exa_field_name=target""",
"""exa_json_path=$.entity_owner_name,exa_field_name=full_name""",
"""exa_json_path=$.entity_owner_email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
"""exa_json_path=$.entity_vendor_name,exa_field_name=process_path""",
"""exa_json_path=$.entity_direct_url,exa_field_name=additional_info""",
"""exa_regex="entity_direct_url":\s*\"({url}[^\"]+)\""""
]
ParserVersion = "v1.0.0"


}
```