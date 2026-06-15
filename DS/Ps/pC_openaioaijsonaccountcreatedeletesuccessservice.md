#### Parser Content
```Java
{
Name = openai-oai-json-account-create-delete-success-service
   ParserVersion = "v1.0.0"
   Conditions = [ """"type":"service_account""", """"effective_at":""", """"actor":""" ]
   Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['service_account.created'].id,exa_field_name=dest_user_id"""
      """exa_json_path=$.['service_account.deleted'].id,exa_field_name=dest_user_id"""
    ]


}
```