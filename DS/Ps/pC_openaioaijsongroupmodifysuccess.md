#### Parser Content
```Java
{
Name = openai-oai-json-group-modify-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"group.updated"""", """"actor":""", """"group.updated":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['group.updated'].id,exa_field_name=group_id"""
      """exa_json_path=$.['group.updated']..group_name,exa_field_name=group_name"""
    ]


}
```