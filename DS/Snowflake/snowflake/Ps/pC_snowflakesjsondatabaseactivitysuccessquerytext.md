#### Parser Content
```Java
{
Name = snowflake-s-json-database-activity-success-querytext
  Vendor = Snowflake
  Product = Snowflake
  TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSS", "yyyy-MM-dd HH:mm:ss.SS"]
  ExtractionType = json
  Conditions = [  """"QUERY_ID":""", """"QUERY_TEXT":""", """"TOTAL_ELAPSED_TIME":""" ]
  Fields = [
    """exa_json_path=$.START_TIME,exa_field_name=time"""
    """exa_json_path=$.QUERY_ID,exa_field_name=query_id"""
    """exa_json_path=$.QUERY_TEXT,exa_field_name=db_query"""
    """exa_json_path=$.SCHEMA_NAME,exa_field_name=db_schema"""
    """exa_json_path=$.DATABASE_NAME,exa_field_name=db_name"""
    """exa_json_path=$.QUERY_TEXT,exa_regex=({db_operation}(?i)(insert|delete|truncate|drop|alter|create|update|enable|disable|merge|select|dbcc))"""
  ]
  ParserVersion = "v1.0.0"


}
```