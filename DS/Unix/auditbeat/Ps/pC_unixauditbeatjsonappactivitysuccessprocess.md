#### Parser Content
```Java
{
Name = "unix-auditbeat-json-app-activity-success-process"
Vendor = "Unix"
Product = "Auditbeat"
ExtractionType = json
TimeFormat = "epoch"
Conditions = [
"""changed-identity-of"""
"""process"""
"""audit_id"""
]
Fields = [
  """exa_json_path=$.time,exa_field_name=time""",
  """exa_json_path=$.hostname,exa_field_name=host""",
  """exa_json_path=$.actor_secondary,exa_field_name=account""",
  """exa_json_path=$.actor_primary,exa_field_name=user""",
  """exa_json_path=$.audit_name,exa_field_name=user""",
  """exa_json_path=$.audit_id,exa_field_name=audit_id""",
  """exa_json_path=$.pid,exa_field_name=process_id""",
  """exa_json_path=$.ppid,exa_field_name=parent_process_id""",
  """exa_json_path=$.title,exa_field_name=process_command_line""",
  """exa_json_path=$.result,exa_field_name=result""",
  """exa_json_path=$.event_type,exa_field_name=operation_type""",
  """exa_json_path=$.category,exa_field_name=category""",
  """exa_json_path=$.syscall,exa_field_name=syscall""",
  """exa_json_path=$.effective_group_id,exa_field_name=group_id""",
  """exa_json_path=$.tags,exa_regex=\[({tags}[^"]+)\]""",
  """exa_json_path=$.os,exa_field_name=os""",
  """exa_json_path=$.application,exa_field_name=app"""
]
ParserVersion = "v1.0.0"


}
```