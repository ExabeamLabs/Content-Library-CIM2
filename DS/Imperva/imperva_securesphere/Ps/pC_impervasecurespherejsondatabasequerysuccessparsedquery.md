#### Parser Content
```Java
{
Name = "imperva-securesphere-json-database-query-success-parsedquery"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = ["dd MMM yyyy HH:mm:ss","dd MMMM yyyy HH:mm:ss"]
ExtractionType = json
Conditions = [
"""Imperva"""
"""db-user"""
"""operation-type"""
"""os-user""""
]
Fields = [
     """exa_json_path=$.source-ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.host-name,exa_field_name=host"""
    """exa_json_path=$.dest-ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.db-user,exa_field_name=db_user"""
    """exa_json_path=$.db-user,exa_field_name=account"""
    """exa_json_path=$.os-user,exa_field_name=user"""
    """exa_json_path=$.operation-type,exa_field_name=db_operation"""
    """exa_json_path=$.parsed-query,exa_field_name=db_query"""
]
ParserVersion = "v1.0.0"


}
```