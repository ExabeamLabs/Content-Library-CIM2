#### Parser Content
```Java
{
Name = "oracle-db-json-database-query-success-oraclefga"
Vendor = "Oracle"
Product = "Oracle Database"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""OracleFGA""""
""""sqlText":"""
]
Fields = [
"""exa_json_path=$.objName,exa_field_name=db_object"""
"""exa_json_path=$.sqlText,exa_field_name=db_query"""
"""exa_json_path=$.objSchema,exa_field_name=db_schema"""
"""exa_json_path=$.@timestamp,exa_field_name=time"""
"""exa_json_path=$.srcHostname,exa_field_name=domain"""
"""exa_json_path=$.action,exa_field_name=db_operation"""
"""exa_json_path=$.instanceName,exa_field_name=db_name"""
"""exa_json_path=$.suUserID,exa_field_name=user"""
"""exa_json_path=$.userID,exa_field_name=db_user"""
]
ParserVersion = "v1.0.0"


}
```