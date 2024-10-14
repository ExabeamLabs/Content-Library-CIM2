#### Parser Content
```Java
{
Name = "postgresql-p-json-database-query-success-databasequery"
Vendor = "PostgreSQL"
Product = "PostgreSQL"
ExtractionType = json
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
""""connection_from":"""
""""error_severity":"""
""""session_line_num":"""
""""sql_state_code":"""
]
Fields = [
  """exa_json_path=$.user_name,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  """exa_json_path=$.log_time,exa_field_name=time""",
  """exa_json_path=$.database_name,exa_field_name=db_name""",
  """exa_json_path=$.process_id,exa_field_name=process_id""",
  """exa_json_path=$.connection_from,exa_field_name=time""",
  """exa_json_path=$.creation_time,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.session_id,exa_field_name=session_id""",
  """exa_json_path=$.transaction_id,exa_field_name=transaction_id""",
  """exa_json_path=$.application_name,exa_field_name=app""",
  """exa_json_path=$.command,exa_field_name=db_operation""",
  """exa_json_path=$.statement,exa_field_name=db_query""",
  """exa_json_path=$.object_name,exa_field_name=db_object""",
  """exa_json_path=$.object_type,exa_field_name=object_type""",
  """exa_json_path=$.error_severity,exa_field_name=severity""",
  """exa_json_path=$.process_id,exa_field_name=process_id""",
  """exa_json_path=$.process_id,exa_field_name=process_id""",
]
DupFields = [
"user->db_user"
]
ParserVersion = "v1.0.0"


}
```