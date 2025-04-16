#### Parser Content
```Java
{
Name = "microsoft-azuread-json-app-login-appdisplayname"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
ExtractionType = json
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSZ"]
Conditions = [ """"userDisplayName": """", """"appDisplayName": """", """"createdDateTime": """" ]
Fields = [
      """exa_json_path=$.time,exa_field_name=time""",
      """exa_json_path=$.operationName,exa_field_name=operation""",
      """exa_json_path=$..createdDateTime,exa_field_name=time""",
      """exa_json_path=$..userPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """exa_json_path=$..ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$..userDisplayName,exa_regex=^(({full_name}({first_name}[^",]+)\s({last_name}[^\s"]+)))$""",
      """exa_json_path=$..userDisplayName,exa_regex=({last_name}[^,"\(]+?)\s*(\([^\)]*\))?,\s*({first_name}[^"\(]+?)\s*(\([^\)]*\))?""",
      """exa_json_path=$..status.failureReason,exa_field_name=failure_reason""",
      """exa_json_path=$..status.errorCode,exa_field_name=error_code""",
      """exa_json_path=$..appDisplayName,exa_field_name=app""",
      """exa_json_path=$..location,exa_field_name=additional_info""",
      """exa_json_path=$..location.city,exa_field_name=location_city""",
      """exa_json_path=$..location.state,exa_field_name=location_state""",
      """exa_json_path=$..location.countryOrRegion,exa_field_name=location_country""",
      """exa_json_path=$..deviceDetail.operatingSystem,exa_field_name=os""",
      """exa_json_path=$..deviceDetail.browser,exa_field_name=browser"""
]
DupFields = ["error_code->failure_code" ]
ParserVersion = "v1.0.0"


}
```