#### Parser Content
```Java
{
Name = "tanium-im-kv-file-write-success-renamepath"
Conditions = [
""" Tanium """
""" Computer-Name =""""
""" Process-Path=""""
""" File-Path=""""
"""Change-Type="RenamePath""""
]
ParserVersion = "v1.0.0"

SSSSSSZ"
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.hostname,exa_field_name=host"""
    """exa_json_path=$.fields.['login__user_name'],exa_field_name=user"""
    """exa_json_path=$.fields.['process__login__user_name'],exa_field_name=user"""
    """exa_json_path=$.event,exa_field_name=event_name"""
    """exa_json_path=$.fields.file__md5,exa_field_name=hash_md5"""
    """exa_json_path=$.fields.parent_pid,exa_field_name=process_id"""
    """exa_json_path=$.fields.command_line,exa_field_name=process_command_line"""
    """exa_json_path=$.fields.['parent__command_line'],exa_field_name=parent_process_command_line"""
    """exa_json_path=$.fields.parent_pid,exa_field_name=parent_process_id"""
  
}
```