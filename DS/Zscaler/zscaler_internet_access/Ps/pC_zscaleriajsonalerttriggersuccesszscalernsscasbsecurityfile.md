#### Parser Content
```Java
{
Name = "zscaler-ia-json-alert-trigger-success-zscalernsscasbsecurityfile"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
time_modifiedFormat = ["EEE MMM dd HH:mm:ss yyyy"]
ExtractionType = json
Conditions = [
""""sourcetype":"zscalernss-casb-security-file""""
""""accesses""""
""""collab_names_int""""
""""collab_names_ext""""
]
Fields = [
"""exa_json_path=$.threatname,exa_field_name=alert_name""",
"""exa_json_path=$.threatname,exa_field_name=alert_type""",
"""exa_json_path=$.dlpdictnames,exa_field_name=dlp_dict""",
"""exa_json_path=$.dept,exa_field_name=department""",
"""exa_json_path=$.applicationname,exa_field_name=app""",
"""exa_json_path=$.login,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
"""exa_json_path=$.policy,exa_field_name=policy_name""",
"""exa_json_path=$.company,exa_field_name=company""",
"""exa_json_path=$.datetime,exa_field_name=time""",
"""exa_json_path=$.tenant,exa_field_name=tenant_id""",
"""exa_json_path=$.fullurl,exa_field_name=url""",
"""exa_json_path=$.filesource,exa_field_name=file_dir""",
"""exa_json_path=$.filename,exa_field_name=file_name""",
"""exa_json_path=$.file_ext,exa_field_name=file_ext""",
"""exa_json_path=$.accesses,exa_field_name=access""",
"""exa_json_path=$.malware_cat,exa_field_name=malware_name""",
"""exa_json_path=$.rulename,exa_field_name=rule""",
"""exa_json_path=$.ruletype,exa_field_name=rule_type""",
"""exa_json_path=$.lastmodtime,exa_field_name=time_modified"""
]
ParserVersion = "v1.0.0"


}
```