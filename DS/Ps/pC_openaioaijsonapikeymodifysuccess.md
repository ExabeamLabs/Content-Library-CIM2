#### Parser Content
```Java
{
Name = openai-oai-json-api-key-modify-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"api_key.updated"""", """"actor":""", """"api_key.updated":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['api_key.updated'].id,exa_field_name=key_id"""
      """exa_json_path=$.['api_key.updated'].changes_requested.scopes,exa_field_name=allowed_permissions"""
      """exa_json_path=$.['api_key.updated'].changes_requested.name,exa_field_name=key_name"""
    ]


}
```