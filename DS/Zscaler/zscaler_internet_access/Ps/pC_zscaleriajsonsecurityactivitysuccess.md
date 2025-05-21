#### Parser Content
```Java
{
Name = "zscaler-ia-json-security-activity-success"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = ["EEE MMM dd HH:mm:ss yyyy","EEE MMM d HH:mm:ss yyyy"]
ExtractionType = json
Conditions = [
""""sourcetype":"zscalernss-casb-security-activity""""
""""activity_time""""
""""activity""""
""""activity_count""""
]
Fields = [
"""exa_json_path=$.datetime,exa_field_name=time""",
"""exa_json_path=$.login,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
"""exa_json_path=$.applicationname,exa_field_name=app""",
"""exa_json_path=$.source_ip,exa_field_name=src_ip""",
"""exa_json_path=$.object_type_1,exa_field_name=object_type""",
"""exa_json_path=$.object_name_1,exa_field_name=object_name""",
"""exa_json_path=$.activity,exa_field_name=action"""
]
ParserVersion = "v1.0.0"


}
```