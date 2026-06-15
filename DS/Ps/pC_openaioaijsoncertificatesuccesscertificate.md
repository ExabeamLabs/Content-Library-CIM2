#### Parser Content
```Java
{
Name = openai-oai-json-certificate-success-certificate
   ParserVersion = "v1.0.0"
   Conditions = [""""type":"certificate.""", """"effective_at":""", """"actor":""" ]
   Fields = ${openaiparsertemplate.openai-json-audit.Fields}[
      """exa_json_path=$.['certificate.created'].name,exa_field_name=object_name"""
      """exa_json_path=$.['certificate.created'].id,exa_field_name=object_id"""
      """exa_json_path=$.['certificate.updated'].name,exa_field_name=object_name"""
      """exa_json_path=$.['certificate.updated'].id,exa_field_name=object_id"""
      """exa_json_path=$.['certificate.deleted'].name,exa_field_name=object_name"""
      """exa_json_path=$.['certificate.deleted'].id,exa_field_name=object_id"""
      """exa_json_path=$.['certificate.deleted'].certificate,exa_field_name=additional_info"""
    ]


}
```