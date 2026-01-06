#### Parser Content
```Java
{
Name = cloudflare-cloudflareaudit-json-app-activity-auditlog
  ExtractionType = json
  Vendor = Cloudflare
  Product = Cloudflare Audit
  TimeFormat = "epoch"
  Conditions = [ """"AccountID":"""", """"ActionType":"""", """"ActionDescription":"""", """"ActionResult":"""", """"AuditLogID":"""" ]
  Fields = [
    """exa_json_path=$.ActionTimestamp,exa_regex=({time}\d{13})"""
    """exa_json_path=$.AccountID,exa_field_name=account_id"""
    """exa_json_path=$.ActionType,exa_field_name=action"""
    """exa_json_path=$.ActorEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.ActionResult,exa_field_name=result"""
    """exa_json_path=$.AccountName,exa_field_name=account_name"""
    """exa_json_path=$.ActorType,exa_field_name=user_type"""
    """exa_json_path=$.ActorIPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.ActionDescription,exa_field_name=operation"""
    """exa_json_path=$.ResourceScope,exa_field_name=object_class"""
    """exa_json_path=$.ResourceProduct,exa_field_name=resource_type"""
    """exa_json_path=$.ResourceID,exa_field_name=resource_id"""
    """exa_json_path=$.ZoneID,exa_field_name=zone_id"""
    """exa_json_path=$.ZoneName,exa_field_name=zone"""
    ]
  ParserVersion = "v1.0.0"


}
```