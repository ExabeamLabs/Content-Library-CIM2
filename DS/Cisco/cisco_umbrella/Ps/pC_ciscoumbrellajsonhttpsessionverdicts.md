#### Parser Content
```Java
{
Name = "cisco-umbrella-json-http-session-verdicts"
Product = "Cisco Umbrella"
Vendor = "Cisco"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
""""Type":"UmbrellaIntelligentProxyLogs"""
"""Verdict_s"""
"""TenantId"""
"""statusCode_s"""
]
Fields = [
"""exa_json_path=$.TimeGenerated,exa_field_name=time"""
"""exa_json_path=$.Computer,exa_field_name=host"""
"""exa_json_path=$.Referer_s,exa_field_name=referrer"""
"""exa_json_path=$.userAgent_s,exa_field_name=user_agent"""
"""exa_json_path=$.Verdict_s,exa_field_name=action"""
"""exa_json_path=$.Categories_s,exa_regex=({category}[^,"]+)?"""
"""exa_json_path=$.Categories_s,exa_field_name=categories"""
"""exa_json_path=$.responseSize_s,exa_field_name=bytes_out"""
"""exa_json_path=$.requestSize_s,exa_field_name=bytes_in"""
"""exa_json_path=$.statusCode_s,exa_field_name=http_response_code"""
"""exa_json_path=$.ContentType_s,exa_field_name=mime"""
"""exa_json_path=$.URL_s,exa_field_name=url"""
"""exa_json_path=$.ExternalIP_s,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""exa_json_path=$.InternalIP_s,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_regex=URL_s"+:"+\s*[^"]+?({uri_query}\?[^\s"]+)"""
"""exa_regex=URL_s"+:"+\s*(?:-|\w+:\/+)({web_domain}[^\s\/"]+)"""
"""exa_regex="+URL_s"+:"+.[^"]+?:\/*([^\/"]+)\/({uri_path}[^\s"]+)"""
]
ParserVersion = "v1.0.0"


}
```