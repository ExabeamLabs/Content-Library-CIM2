#### Parser Content
```Java
{
Name = microsoft-azureadactivity-json-user-mfa-modify-fail-adminregister
  Conditions = [ """"activityDisplayName":"Admin registered security info"""", """"resultReason":"Admin failed to register phone method for user"""" ]
  Fields = ${MSParserTemplates.azure-ad-activity-json.Fields}[
    """exa_json_path=$..resultReason,exa_field_name=failure_reason""",
  ]
  ParserVersion = "v1.0.0"

azure-ad-activity-json = {
    Vendor = Microsoft
    Product = Azure AD Activity Logs
    ExtractionType = json
    TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
    Fields = [
      """exa_json_path=$..activityDateTime,exa_field_name=time""",
      """exa_json_path=$..activityDisplayName,exa_field_name=event_name""",
      """exa_json_path=$..resultReason,exa_field_name=result_reason""",
      """exa_json_path=$..result,exa_field_name=result""",
      """exa_json_path=$..category,exa_field_name=event_category""",
      """exa_json_path=$..initiatedBy.user.id,exa_field_name=user_id""",
      """exa_json_path=$..initiatedBy.user.userPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
      """exa_json_path=$..initiatedBy..ipAddress,exa_field_name=src_ip""",
      """exa_json_path=$..targetResources[*].userPrincipalName,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[^@",\s]+))""",
      """exa_json_path=$..targetResources[*].userPrincipalName,exa_regex=({dest_user}[^@\"]+)""",
      """exa_json_path=$..modifiedProperties[?(@.displayName == 'Phone.Phone.Id')].newValue,exa_field_name=device_id""",
      """exa_json_path=$..modifiedProperties[?(@.displayName == 'Phone.Phone.Id')].oldValue,exa_field_name=old_value""",
      """exa_json_path=$..modifiedProperties[?(@.displayName == 'Phone.Phone.PhoneType')].newValue,exa_field_name=device_type"""
    
}
```