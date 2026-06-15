#### Parser Content
```Java
{
Name = openai-oai-json-user-delete-success-userdeleted
   ParserVersion = "v1.0.0"
   Conditions = [""""type":"user.deleted"""", """"effective_at":""", """"actor":""" ]
   Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['user.deleted'].id,exa_field_name=dest_user_id"""
    ]


}
```