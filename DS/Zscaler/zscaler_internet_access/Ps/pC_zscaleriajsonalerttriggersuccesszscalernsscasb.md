#### Parser Content
```Java
{
Name = "zscaler-ia-json-alert-trigger-success-zscalernsscasb"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
ExtractionType = json
Conditions = [
""""zscalernss-casb""""
""""dlpenginenames":"""
""""recordid":"""
""""company":"""
]
Fields = [
"""exa_json_path=$.event.threatname,exa_field_name=alert_name,exa_match_expr=!InList($.event.threatname,"None")""",
"""exa_json_path=$.event.dlpdictnames,exa_field_name=dlp_dict,exa_match_expr=!InList($.event.dlpdictnames,"None")""",
"""exa_json_path=$.event.dept,exa_field_name=department""",
"""exa_json_path=$.event.applicationname,exa_field_name=app""",
"""exa_json_path=$.event.login,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
"""exa_json_path=$.event.owner,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
"""exa_json_path=$.event.policy,exa_field_name=policy_name,exa_match_expr=!InList($.event.policy,"None")""",
"""exa_json_path=$.event.company,exa_field_name=company""",
"""exa_json_path=$.event.bucket_name,exa_field_name=bucket_name""",
"""exa_json_path=$.event.datetime,exa_field_name=time""",
"""exa_json_path=$.event.tenant,exa_field_name=tenant_id""",
"""exa_json_path=$.event.fullurl,exa_field_name=url""",
"""exa_json_path=$.event.filesource,exa_field_name=file_path""",
"""exa_json_path=$.event.filename,exa_field_name=file_name"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```