#### Parser Content
```Java
{
Name = openai-oai-json-role-create-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"role.created"""", """"actor":""", """"role.created":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['role.created'].id,exa_field_name=role_id"""
      """exa_json_path=$.['role.created'].role_name,exa_field_name=role_name"""
    ]


}
```