#### Parser Content
```Java
{
Name = openai-oai-json-group-delete-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"group.deleted"""", """"actor":""", """"group.deleted":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['group.deleted'].id,exa_field_name=group_id"""
      """exa_json_path=$.['group.deleted'].name,exa_field_name=group_name"""
    ]


}
```