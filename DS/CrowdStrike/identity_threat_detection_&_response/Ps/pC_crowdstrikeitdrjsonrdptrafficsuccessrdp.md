#### Parser Content
```Java
{
Name = "crowdstrike-itdr-json-rdp-traffic-success-rdp"
  Vendor = "CrowdStrike"
  Product = "Identity Threat Detection & Response"
  ExtractionType = json
  Conditions = [ """"eventType": "SERVICE_ACCESS"""", """"eventLabel": "Remote Desktop (RDP)"""", """"targetServiceType": "REMOTE_DESKTOP"""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.eventType,exa_field_name=event_category""",
    """exa_json_path=$.eventLabel,exa_field_name=event_name""",
    """exa_json_path=$.eventSeverity,exa_field_name=alert_severity"""
    """exa_json_path=$.endpointDisplayName,exa_field_name=src_host"""
    """exa_json_path=$.userEntity.primaryDisplayName,exa_field_name=full_name"""
    """exa_json_path=$.userEntity.secondaryDisplayName,exa_regex=(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """exa_json_path=$.targetEntity.primaryDisplayName,exa_field_name=dest_host"""
    """exa_json_path=$.targetServiceType,exa_field_name=tgs_service_name"""
    """exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$.userEntity.emailAddresses,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```