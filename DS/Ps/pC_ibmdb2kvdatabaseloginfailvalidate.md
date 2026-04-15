#### Parser Content
```Java
{
Name = ibm-db2-kv-database-login-fail-validate
Conditions = [
  """; category=VALIDATE; """
  """; audit event=AUTHENTICATION; """
  """; database="""
  """; userid="""
]
ParserVersion = "v1.0.0"

SS Z"
    Fields = [
      """exa_json_path=$.DATETIME,exa_field_name=time""",
      """exa_json_path=$.ACTION,exa_field_name=severity""",
      """exa_json_path=$.MSGNUM,exa_field_name=event_code""",
      """exa_json_path=$.MSGTXT,exa_field_name=additional_info"""
    
}
```