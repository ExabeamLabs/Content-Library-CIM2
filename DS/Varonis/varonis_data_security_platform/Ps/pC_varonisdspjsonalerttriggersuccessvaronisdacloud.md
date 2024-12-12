#### Parser Content
```Java
{
Name = "varonis-dsp-json-alert-trigger-success-varonisdacloud"
 Vendor = "Varonis"
 Product = "Varonis Data Security Platform"
 ExtractionType = json
 TimeFormat = "MMM dd, yyyy HH:mm:ss" 
 Conditions = [ """"type":"Varonis DA Cloud"""", """"title":""", """"description":""", """"Affected Target(s)":""", """"Actor(s)":""" ]
 Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.policy_id.['Policy name/rule name triggered'],exa_field_name=alert_name"""
    """exa_json_path=$.policy_id.Category,exa_field_name=alert_type"""
    """exa_json_path=$.title,exa_field_name=alert_description"""
    """exa_json_path=$.description,exa_field_name=additional_info"""
    """exa_json_path=$.['Actor(s)']..actor_name,exa_regex=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^":]+))"""
    """exa_json_path=$.['Affected Target(s)']..target_name,exa_field_name=dest_user_full_name,exa_match_expr=Contains($.['Affected Target(s)']..target_type,"user")"""
    """exa_json_path=$.['Affected Target(s)']..target_name,exa_field_name=file_name,exa_match_expr=Contains($.['Affected Target(s)']..target_type,"file")"""
 ]
 ParserVersion = "v1.0.0"


}
```