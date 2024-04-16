#### Parser Content
```Java
{
Name = microsoft-sentinel-json-group-member-add-success-addmembertogroup
    ParserVersion = v1.0.0
    Conditions = [ """"Type":"BehaviorAnalytics"""", """"ActivityType":"GroupManagement"""", """"Add member to group"""" ]
    Fields = ${MicrosoftSentinelJsonTemplates.microsoft-sentinel.Fields}[
      """exa_json_path=$.ActivityInsights.UserAdded,exa_field_name=dest_email_address({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    ]

microsoft-sentinel = {
    Vendor = Microsoft
    Product = Microsoft Sentinel
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Fields=[
      """exa_json_path=$.TimeGenerated,exa_field_name=time"""
      """exa_json_path=$.SourceIPAddress,exa_field_name=src_ip"""
      """exa_json_path=$.UserName,exa_field_name=user"""
      """exa_json_path=$.ActivityType,exa_field_name=operation"""
      """exa_json_path=$.$.UsersInsights.AccountObjectID,exa_field_name=object"""
      """exa_json_path=$.UserPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """exa_json_path=$.SourceIPLocation,exa_field_name=location"""
      """exa_json_path=$.TenantId,exa_field_name=tenant_id"""
      """exa_json_path=$.ActivityInsights.App,exa_field_name=app"""
      """exa_json_path=$.ActivityType,exa_field_name=category"""
      """exa_json_path=$.UsersInsights.AccountDisplayName,exa_field_name=full_name"""
    
}
```