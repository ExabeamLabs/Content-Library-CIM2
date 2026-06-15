#### Parser Content
```Java
{
Name = openai-oai-json-role-assign-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"role.assignment.created"""", """"actor":""", """"role.assignment.created":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['role.assignment.created'].id,exa_field_name=role_id"""
      """exa_json_path=$.['role.assignment.created'].principal_type,exa_field_name=object_type"""
      """exa_json_path=$.['role.assignment.created'].principal_id,exa_field_name=object_id"""
      """exa_json_path=$..[?(@.principal_type == 'user')].principal_id,exa_field_name=dest_user_id"""
      """exa_json_path=$..[?(@.principal_type == 'group')].principal_id,exa_field_name=group_id"""
    ]


}
```