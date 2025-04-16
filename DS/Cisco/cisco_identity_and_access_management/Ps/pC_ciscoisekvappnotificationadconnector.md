#### Parser Content
```Java
{
Name = "cisco-ise-kv-app-notification-adconnector"
  Vendor = "Cisco"
  Product = "Cisco Identity and Access Management"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ CISE_AD_Connector """
   ]
  Fields = [
    """({host}[^\s]+)\s*CISE_AD_Connector"""
    """({event_name}CISE_AD_Connector)"""
# ad_domain_controller is removed
    """AD-Connector:\s*({result}[^,]+)"""
    """AD-Domain=\s*({domain}[^,]+)"""
    """AD-Log-Id=\s*({event_id}[^,]+)"""
    """AD-Srv-Query=\s*({query}[^,]+)"""
# ad_srv_record is removed
# ad_srv_record is removed
    """AD-Site=\s*({site_state}[^,]+)"""
    """AD-Hostname=\s*({host}[^,]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```