#### Parser Content
```Java
{
Name = microsoft-o365-json-app-consent-grant-success-operation
  Conditions = [ """"Operation":"Consent to application."""", """Workload""" ]
  Fields = ${MSParserTemplates.m365-activity-json.Fields}[
    """exa_regex="NewValue":[^\}]+ConsentType:\s+({principal_type}[^:,]+),\s+Scope:\s+({permission}[^:,]+)[^\}]+"Name":"ConsentAction\.Permissions""""
    """exa_regex="Name":"ConsentAction\.Permissions"[^\}]+"NewValue":[^\}]+ConsentType:\s+({principal_type}[^:,]+),\s+Scope:\s+({permission}[^:,]+)"""
    """exa_regex="Target":\[([^\}]+},){3}\{"ID":"({app}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"

m365-activity-json = {
    Vendor = Microsoft
    Product = Microsoft 365
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """exa_json_path=$.CreationTime,exa_field_name=time"""
      """exa_json_path=$.OriginatingServer,exa_field_name=host"""
      """exa_json_path=$.Operation,exa_field_name=operation"""
      """exa_regex=\ssuser=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(NOT-FOUND|Unknown|Sync|AirInvestigation|Sync Client|Office365 Backend Process|Device Registration Service|Microsoft Intune|Microsoft Teams Services|Microsoft Online Services|Office 365 SharePoint Online|anonymous|SecurityComplianceAlerts|SecurityComplianceInsights|(Microsoft\\[^@\s"]+)|EMPTY\.*|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s@"]+)\\+)(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[^",]+)))"""
      """exa_regex="UserId":"((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|(NOT-FOUND|Unknown|Sync|AirInvestigation|Sync Client|Office365 Backend Process|Device Registration Service|Microsoft Intune|Microsoft Teams Services|Microsoft Online Services|Office 365 SharePoint Online|anonymous|SecurityComplianceAlerts|SecurityComplianceInsights|(Microsoft\\[^@\s"]+)|EMPTY\.*|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s@"]+)\\+)(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[^",]+)))"""
      """exa_regex=\sfname=\s*({object}[^=]+?)\s*(\w+=|$)"""
      """exa_regex="User-?Agent\\?":\s*\\?"({user_agent}[^"\}:]+?)\\?""""
      """exa_json_path=$.SourceFileName,exa_field_name=object"""
      """exa_json_path=$.ObjectId,exa_field_name=object_id"""
      """exa_json_path=$.ClientIP,exa_field_name=src_ip"""
      """exa_json_path=$.ClientIPAddress,exa_field_name=src_ip"""
      """exa_json_path=$.Workload,exa_field_name=service_name"""
      """exa_json_path=$.ApplicationId,exa_field_name=app_id"""
      """exa_json_path=$.result,exa_field_name=result"""
      """exa_json_path=$.ResultStatus,exa_field_name=result"""
      """exa_json_path=$.AADSessionId,exa_field_name=session_id"""
      """exa_json_path=$.SessionId,exa_field_name=session_id"""
    
}
```