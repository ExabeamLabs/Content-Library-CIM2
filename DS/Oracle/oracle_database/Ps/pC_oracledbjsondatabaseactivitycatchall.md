#### Parser Content
```Java
{
Name = oracle-db-json-database-activity-catchall
  Vendor = Oracle
  Product = Oracle Database
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd HH:mm:ss.S", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss.SSSSS", "yyyy-MM-dd HH:mm:ss.SSSSSS"]
  Conditions = [ """action_name""", """"os_username""", """userhost""", """dbid""", """returncode""" ]
  Fields=[
    """exa_json_path=$.os_username,exa_field_name=user"""
    """exa_json_path=$.username,exa_field_name=db_user"""
    """exa_json_path=$.action_name,exa_field_name=operation""",
    """exa_json_path=$.action_name,exa_field_name=db_operation""",
    """exa_json_path=$.sessionid,exa_field_name=session_id""",
    """exa_json_path=$.userhost,exa_regex=(({domain}[^\\]+)[\\]+)?({host}[^"]+)"""
    """exa_json_path=$.os_process,exa_field_name=process_id""",
    """exa_json_path=$.event_timestamp,exa_field_name=time""",
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.exa_jdbc_database,exa_field_name=db_name""",
    """exa_json_path=$.priv_used,exa_field_name=additional_info""",
    """exa_json_path=$.exa_jdbc_type,exa_field_name=app""",
    """exa_json_path=$.exa_jdbc_hostname,exa_field_name=dest_host""",
    """exa_json_path=$.exa_jdbc_port,exa_field_name=dest_port"""
  ]


}
```