#### Parser Content
```Java
{
Name = openai-oai-json-api-key-delete-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"api_key.deleted"""", """"actor":""", """"api_key.deleted":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['api_key.deleted'].id,exa_field_name=key_id"""
    ]


}
```