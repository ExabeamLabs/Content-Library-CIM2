#### Parser Content
```Java
{
Name = openai-oai-json-role-modify-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"role.updated"""", """"actor":""", """"role.updated":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['role.updated'].id,exa_field_name=role_id"""
      """exa_json_path=$.['role.updated']..role_name,exa_field_name=role_name"""
      """exa_json_path=$.['role.updated']..permissions_added,exa_field_name=allowed_permissions"""
    ]


}
```