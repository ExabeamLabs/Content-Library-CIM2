#### Parser Content
```Java
{
Name = openai-oai-json-app-activity-success-projectcreated
   ParserVersion = "v1.0.0"
   Conditions = [""""type":"project.created"""", """"ja3":""", """"ja4":""", """project.created"""]
   Fields = ${OpenAIParserTemplates.openaievents.Fields} [
     """exa_json_path=$.project.created.id,exa_field_name=project_id"""
   ]
 
openaievents = {
    Vendor = OpenAI
    Product = OpenAI
    ExtractionType = json
    TimeFormat = "epoch_sec"
    Fields = [
      """exa_json_path=$.effective_at,exa_field_name=time""",
      """exa_json_path=$.type,exa_field_name=event_name""",
      """exa_json_path=$.actor.session.user.id,exa_field_name=user_id""",
      """exa_json_path=$.actor.session.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """exa_json_path=$.actor.session.ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
      """exa_json_path=$.actor.session.user_agent,exa_field_name=user_agent""",
      """exa_json_path=$.actor.session.ip_address_details.country,exa_field_name=country_code""",
      """exa_json_path=$.actor.session.ip_address_details.city,exa_field_name=city""",
      """exa_json_path=$.actor.session.ip_address_details.region,exa_field_name=region"""
    
}
```