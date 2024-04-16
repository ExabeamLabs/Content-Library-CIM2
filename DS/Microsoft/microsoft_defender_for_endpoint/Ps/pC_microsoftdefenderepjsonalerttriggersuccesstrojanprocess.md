#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-alert-trigger-success-trojanprocess"
ExtractionType = json
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""threatname":""""
""""scepmaldetecttime":""""
]
Fields = [
"""exa_json_path=$.username,exa_field_name=user_id"""
"""exa_json_path=$.threatname,exa_field_name=alert_name"""
"""exa_json_path=$.threatid,exa_field_name=threat_id"""
"""exa_json_path=$.targethost,exa_field_name=src_host"""
"""exa_json_path=$.severityid,exa_field_name=alert_severity"""
"""exa_json_path=$.process,exa_regex=(({process_path}({process_dir}[^"]+[\\\/]+))?({process_name}[^"]+))"""
"""exa_json_path=$.path,exa_field_name=malware_url"""
"""exa_json_path=$.ntdomain,exa_field_name=domain"""
"""exa_json_path=$.name,exa_field_name=alert_type"""
"""exa_json_path=$.maliciousfilect,exa_field_name=malicious_file_count"""
"""exa_json_path=$.mal_id,exa_field_name=malware_id"""
"""exa_json_path=$.executionstatus,exa_field_name=execution_status"""
"""exa_json_path=$.errorcode,exa_field_name=error_code"""
"""exa_json_path=$.cleanaction,exa_field_name=result"""
"""exa_json_path=$.category,exa_field_name=threat_category"""
"""exa_json_path=$.actionsuccess,exa_field_name=result"""
"""exa_json_path=$.@version,exa_field_name=version"""
"""exa_json_path=$.scepmaldetecttime,exa_field_name=time"""
]
ParserVersion = "v1.0.0"


}
```