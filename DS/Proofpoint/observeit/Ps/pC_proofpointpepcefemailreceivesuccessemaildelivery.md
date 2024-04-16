#### Parser Content
```Java
{
Name = "proofpoint-pep-cef-email-receive-success-emaildelivery"
Conditions = [
  """CEF:"""
  """|ProofPoint|"""
  """|Email Delivery In|"""
]
ParserVersion = "v1.0.0"

observeit-activity = {
  Vendor = Proofpoint
  Product = ObserveIT
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Fields = [
      """exa_json_path=$.observedAt,exa_field_name=time""",
      """exa_json_path=$.applicationName,exa_regex=(?:[A-Fa-f:\d.]+|({app}[^"]+))""",
      """exa_json_path=$.command,exa_field_name=command""",
      """exa_json_path=$.domainName,exa_field_name=domain""",
      """exa_json_path=$.endpointName,exa_field_name=host""",
      """exa_json_path=$.loginName,exa_regex=({user}[\w\.\-]{1,40}\$?)$""",
      """exa_json_path=$.loginName,exa_regex=({full_name}\w+\s\w+)""",
      """exa_json_path=$.os,exa_field_name=os""",
      """exa_json_path=$.remoteAddress,exa_regex=(?:127\.0\.0\.1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
      """exa_json_path=$.remoteHostName,exa_regex=(?:\(local\)|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^",]+))""",
      """exa_json_path=$.ruleCategoryName,exa_field_name=alert_type""",
      """exa_json_path=$.ruleName,exa_field_name=alert_name""",
      """exa_json_path=$.severity,exa_field_name=alert_severity""",
      """exa_json_path=$.sessionId,exa_field_name=session_id""",
      """exa_json_path=$.ruleDesc,exa_field_name=additional_info""",
      """exa_json_path=$.detailsUrl,exa_field_name=additional_info""",
      """exa_json_path=$.sqlUserName,exa_field_name=db_user""",
      """exa_json_path=$.databaseName,exa_field_name=db_name""",
      """exa_json_path=$.id,exa_field_name=alert_id""",
  
}
```