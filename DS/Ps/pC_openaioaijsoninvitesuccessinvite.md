#### Parser Content
```Java
{
Name = openai-oai-json-invite-success-invite
   ParserVersion = "v1.0.0"
   Conditions = [ """"type":"invite.""", """"effective_at":""", """"actor":""" ]
   Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['invite.sent']..email,exa_field_name=dest_email_address"""
      """exa_json_path=$.['invite.sent']..role,exa_field_name=role_name"""
      """exa_json_path=$.['invite.sent']..id,exa_field_name=transaction_id"""
      """exa_json_path=$.['invite.accepted']..id,exa_field_name=transaction_id"""
      """exa_json_path=$.['invite.deleted']..id,exa_field_name=transaction_id"""
   ]


}
```