#### Parser Content
```Java
{
Name = openai-oai-json-group-create-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"group.created"""", """"actor":""", """"group.created":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['group.created'].id,exa_field_name=group_id"""
      """exa_json_path=$.['group.created'].name,exa_field_name=group_name"""
    ]


}
```