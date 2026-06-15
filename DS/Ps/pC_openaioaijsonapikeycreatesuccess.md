#### Parser Content
```Java
{
Name = openai-oai-json-api-key-create-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"api_key.created"""", """"actor":""", """"api_key.created":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['api_key.created'].id,exa_field_name=key_id"""
      """exa_json_path=$.['api_key.created'].data.scopes,exa_field_name=allowed_permissions"""
    ]


}
```