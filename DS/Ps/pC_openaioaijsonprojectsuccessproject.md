#### Parser Content
```Java
{
Name = openai-oai-json-project-success-project
   ParserVersion = "v1.0.0"
   Conditions = [""""type":"project.""", """"effective_at":""", """"actor":""" ]
   Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['project.updated'].id,exa_field_name=project_id"""
      """exa_json_path=$.['project.updated']..title,exa_field_name=project_name"""
      """exa_json_path=$.['project.archived'].id,exa_field_name=project_id"""
    ]


}
```