#### Parser Content
```Java
{
Name = ibm-racf-kv-database-activity-success-access
Conditions = [
  """EVNTPRODESCR=VANGUARD_ACTIVE_ALERTS"""
  """EVNTNAME=Access"""
  """EVNTTEXT=Failed due to PROTECTALL"""
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