#### Parser Content
```Java
{
Name = "cisco-umbrella-json-dns-response-success-identities"
Vendor = "Cisco"
Product = Cisco Cloud Security
ExtractionType = json
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""MostGranularIdentity""""
""""Identities""""
""""QueryType""""
""""ResponseCode""""
]
Fields = [
""""(Timestamp|timestamp)"*:\"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""Identities"*:\"*({identities}[^\"]+)"""
""""InternalIp"*:\"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""ExternalIp"*:\"*({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?"""
""""Action"*:\"*({result}[^\"]+)"""
""""QueryType"*:\"*({dns_query_type}[^\"]+)"""
""""ResponseCode"*:\"*({dns_response_code}[^\"]+)"""
""""Domain"*:\"*({dns_query}[^\"]+)"""
""""categories":\[({categories}({category}[^,;]+)[^\]]+)"""
"""exa_json_path=$.Timestamp,exa_field_name=time"""
"""exa_json_path=$.Identities,exa_field_name=identities"""
"""exa_json_path=$.InternalIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.ExternalIp,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?"""
"""exa_json_path=$.Action,exa_field_name=result"""
"""exa_json_path=$.QueryType,exa_field_name=dns_query_type"""
"""exa_json_path=$.ResponseCode,exa_field_name=dns_response_code"""
"""exa_json_path=$.Domain,exa_field_name=dns_query"""
"""exa_regex="Categories"*:"*({categories}({category}[^,"]+)[^"]*)""""
]
ParserVersion = "v1.0.0"


}
```