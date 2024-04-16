#### Parser Content
```Java
{
Name = azure-azuremfa-json-app-activity-additionaldetails
  ParserVersion = "v1.0.0"
  Conditions = [ """"additionalDetails":"""", """"resourceId":"""", """"conditionalAccessStatus":"""" ]
  Fields = ${MicrosoftParserTemplates.microsoft-azuremfa-json-events.Fields}[
    """exa_json_path=$.status.failureReason,exa_field_name=failure_reason"""
    """exa_json_path=$.status.errorCode,exa_field_name=error_code"""
    """exa_json_path=$.conditionalAccessStatus,exa_field_name=result"""
 ]

microsoft-azuremfa-json-events = {
    Vendor = Microsoft
    Product = Azure MFA
    ExtractionType = json
    TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSZ","yyyy-MM-dd'T'HH:mm:ssZ" ]
    Fields = [
      """exa_json_path=$.createdDateTime,exa_field_name=time""",
      """exa_json_path=$.userDisplayName,exa_field_name=full_name""",
      """exa_json_path=$.userId,exa_field_name=user_uid""",
      """exa_json_path=$.resourceId,exa_field_name=resource_id""",
      """exa_json_path=$.deviceDetail.displayName,exa_field_name=host,exa_match_expr=!InList($.deviceDetail.displayName,"")"""
      """exa_json_path=$.appDisplayName,exa_field_name=app""",
      """exa_regex="ipAddress":"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
      """exa_json_path=$.userPrincipalName,exa_field_name=dest_email_address""",
      """exa_json_path=$.userPrincipalName,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^@",\s]+))"""",
      """exa_json_path=$.status.additionalDetails,exa_field_name=event_name""",
      """exa_json_path=$.correlationId,exa_field_name=correlation_id""",
      """exa_json_path=$.location.countryOrRegion,exa_field_name=location_country""",
      """exa_json_path=$.location.state,exa_field_name=location_state"""
    ]
    DupFields = ["location_country->mfa_country"
}
```