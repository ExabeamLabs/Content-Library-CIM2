#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-storageblonapplicationanomoly
  Conditions = [ """"category":""", """"Storage.Blob_ApplicationAnomaly"""", """"createdDateTime":""", """"eventDateTime":""", """"azureTenantId":""", """"status":""", """"title":""" ]

json-atp-alert = {
  Vendor = Microsoft
  Product = Azure ATP
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
    """exa_json_path=$.id,exa_field_name=alert_id"""
    """exa_json_path=$.category,exa_field_name=alert_type"""
    """exa_json_path=$.eventDateTime,exa_field_name=time""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.status,exa_field_name=incident_status"""
    """exa_json_path=$.title,exa_field_name=alert_name"""
    """exa_json_path=$.hostStates[:1].fqdn,exa_field_name=host"""
    """exa_json_path=$.recommendedActions,exa_field_name=remediation_steps"""
    """exa_regex=(?i)"resource":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^"]+?))?(\/({resource}[^"\/]+))?)""""
    """exa_json_path=$.userStates[:1].logonIp,exa_field_name=src_ip"""
    """exa_json_path=$.userStates[:1].logonLocation,exa_field_name=location"""
    """exa_regex="userStates":\s*[^\]]+?"userPrincipalName":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^"]+))""""
    """exa_regex="Operations types\\*":\\*"({operation_type}[^\\"]+)"""
    """exa_regex="Service type\\*":\\*"({service_type}[^\\"]+)"""
    """exa_regex="User agent\\*":\\*"({user_agent}[^\\"]+)"""
  
}
```