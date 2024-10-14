#### Parser Content
```Java
{
Name = pingidentity-pingone-json-user-role-assign-success-roleassignmentcreated
  ParserVersion = "v1.0.0"
  Conditions = [  """"type":"ROLE_ASSIGNMENT.CREATED"""", """"actors":""", """"action":""", """"resources":""", """"internalCorrelation":""" ]

pingone-events = {
   Vendor = Ping Identity
   Product = PingOne
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   ExtractionType = json
   Fields = [
      """exa_json_path=$.recordedAt,exa_field_name=time""",
      """exa_json_path=$.action.type,exa_field_name=operation""",
      """exa_json_path=$.action.description,exa_field_name=event_name""",
      """exa_json_path=$.source.userAgent,exa_field_name=user_agent""",
      """exa_json_path=$.actors.client.name,exa_field_name=client_name""",
      """exa_json_path=$.actors.client.id,exa_field_name=client_id""",
      """exa_json_path=$.actors.client.type,exa_field_name=client_type""",
      """exa_json_path=$.result.status,exa_field_name=result""",
      """exa_json_path=$.result.description,exa_field_name=additional_info""",
      """exa_json_path=$.correlationId,exa_field_name=correlation_id""",
      """exa_json_path=$.source.ipAddress,exa_field_name=src_ip""",
      """exa_regex="user":.+?"name":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """exa_regex="resources":.+?"name":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
   
}
```