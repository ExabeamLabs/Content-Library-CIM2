#### Parser Content
```Java
{
Name = azure-azuread-json-app-authentication-updatestsrefreshtokenvalidfromtimestamp
  ParserVersion = "v1.0.0"
  Conditions = [ """"activityDisplayName":"Update StsRefreshTokenValidFrom Timestamp"""", """"operationType":"Update"""", """"targetResources":""", """"category":"UserManagement"""" ]
  Fields = ${MicrosoftParserTemplates.microsoft-azuread-json-events.Fields}[
    """exa_json_path=$.targetResources[:1].userPrincipalName,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^@",\s]+))"""",
    """exa_json_path=$.targetResources[:1].id,exa_field_name=user_sid""",
    """exa_json_path=$.activityDisplayName,exa_field_name=operation"""
  ]

microsoft-azuread-json-events = {
    Vendor = Microsoft
    Product = Azure AD Activity Logs
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
    Fields = [
      """exa_json_path=$..activityDateTime,exa_field_name=time""",
      """exa_json_path=$..initiatedBy.user.userPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """exa_json_path=$..initiatedBy.user.id,exa_field_name=user_uid""",
      """exa_regex="initiatedBy":\s*\{[^\]]+?ipAddress":\s*"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
      """exa_json_path=$..result,exa_field_name=result"""
      """exa_json_path=$.category,exa_field_name=category""",
      """exa_json_path=$[?(@.loggedByService nin ['Core Directory','Account Provisioning'])].loggedByService,exa_field_name=app""",
      """exa_json_path=$..initiatedBy.app.displayName,exa_field_name=app""",
      """exa_regex=resultReason":"({additional_info}[^"]+)""""
      """exa_json_path=$..operationType,exa_field_name=operation""",
      """exa_json_path=$..correlationId,exa_field_name=correlation_id""",
      """exa_json_path=$..activityDisplayName,exa_field_name=event_name"""
      """exa_json_path=$..ActivityDateTime,exa_field_name=time""",
      """exa_json_path=$..InitiatedBy.user.userPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """exa_json_path=$..InitiatedBy.user.id,exa_field_name=user_uid""",
      """exa_regex="InitiatedBy":\s*\{[^\]]+?ipAddress":\s*"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
      """exa_json_path=$..Result,exa_field_name=result"""
      """exa_json_path=$.Category,exa_field_name=category""",
      """exa_json_path=$[?(@.LoggedByService nin ['Core Directory','Account Provisioning'])].LoggedByService,exa_field_name=app""",
      """exa_json_path=$..InitiatedBy.app.displayName,exa_field_name=app""",
      """exa_json_path=$.ResultReason,exa_field_name=additional_info""",
      """exa_json_path=$..AADOperationType,exa_field_name=operation""",
      """exa_json_path=$..CorrelationId,exa_field_name=correlation_id""",
      """exa_json_path=$..ActivityDisplayName,exa_field_name=event_name""",

      """"activityDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+([+-]\d\d:\d\d|Z))"""",
      """"initiatedBy":[^\}]+?userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
      """"initiatedBy":[^\}]+?id":"({user_uid}[^",]+)"""",
      """"initiatedBy":\{[^\}]+?ipAddress":"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
      """"callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"result":"({result}[^"]+)"""",
      """"resultReason":"({result_reason}[^"]+)"""",
      """"category":"({category}[^"]+)"""",
      """"properties".*?"category":"({category}[^"]+)"""",
      """"loggedByService":"(Account Provisioning|Core Directory|({app}[^"]+))"""",
      """"initiatedBy":\{"app":\{[^\}]*?"displayName":"({app}[^"]+)"""",
      """"operationType":"({operation}[^"]+)"""",
      """"correlationId":"({correlation_id}[^"]+)"""",
      """"activityDisplayName":"({operation}({event_name}[^"]+))"""",
      """"targetResources":\[\{[^\}]+?userPrincipalName":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^"]+))""""
    
}
```