#### Parser Content
```Java
{
Name = oracle-db-kv-app-activity-sqlbind
  Vendor = Oracle
  Product = Oracle Database
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"userhost":""",""""sqlbind":""",""""auditid":""" ]
  Fields = [
    """exa_json_path=$.ntimestamp#,exa_field_name=time"""
    """exa_json_path=$.userhost,exa_regex=(({domain}[^\\]+)[\\]+)?({host}[^"]+)"""
    """exa_json_path=$.userid,exa_field_name=db_user""",
    """exa_json_path=$.sessionid,exa_field_name=session_id""",
    """exa_json_path=$.dbid,exa_field_name=db_id""",
# action_code is removed
    """exa_json_path=$.comment$text,exa_field_name=additional_info"""
  ]
  DupFields = [ "db_user->user" ]


}
```