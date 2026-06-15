#### Parser Content
```Java
{
Name = openai-oai-json-role-delete-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"role.deleted"""", """"actor":""", """"role.deleted":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['role.deleted'].id,exa_field_name=role_id"""
      """exa_json_path=$.['role.deleted'].role_name,exa_field_name=role_name"""
    ]


}
```