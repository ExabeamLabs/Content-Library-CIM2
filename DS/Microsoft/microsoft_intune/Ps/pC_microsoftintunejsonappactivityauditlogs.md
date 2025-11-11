#### Parser Content
```Java
{
Name = microsoft-intune-json-app-activity-auditlogs
  ExtractionType = json
  Conditions= [ """"category":"AuditLogs"""", """"operationName":"""", """"Actor":""", """"Targets":""" ]
  ParserVersion = "v1.0.0"

ms-intune-app-activity = {
  Vendor = Microsoft
  Product = Microsoft Intune
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.operationName,exa_field_name=operation""",
    """exa_json_path=$.operationName,exa_field_name=event_name""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.resultType,exa_field_name=result,exa_match_expr=!Contains($.resultType,"None")""",
    """exa_json_path=$..Actor.ApplicationName,exa_field_name=app""",
    """exa_json_path=$..Actor.UPN,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$..Targets[:1].Name,exa_field_name=target""",
    """exa_json_path=$..UserEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$..UserName,exa_field_name=full_name,exa_match_expr=!Contains($..UserName,"")""",
    """exa_json_path=$..DeviceName,exa_field_name=host""",
    """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
  
}
```