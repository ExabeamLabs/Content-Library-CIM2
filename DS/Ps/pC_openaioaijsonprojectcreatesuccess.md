#### Parser Content
```Java
{
Name = openai-oai-json-project-create-success
  ParserVersion = v1.0.0
  Conditions = [ """"type":"project.created"""", """"actor":""", """"project.created":""", """"effective_at":""" ]
  Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['project.created'].id,exa_field_name=project_id"""
      """exa_json_path=$.['project.created']..title,exa_field_name=project_name"""
    ]


}
```