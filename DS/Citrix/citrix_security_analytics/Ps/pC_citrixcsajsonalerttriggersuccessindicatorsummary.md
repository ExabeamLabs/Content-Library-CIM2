#### Parser Content
```Java
{
Name = citrix-csa-json-alert-trigger-success-indicatorsummary
  Vendor = Citrix
  Product = Citrix Security Analytics
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"indicator_id":"""", """"indicator_category":"""", """"event_type":"indicatorSummary"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.event_type,exa_field_name=event_name""",
    """exa_json_path=$.entity_id,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.indicator_category,exa_field_name=alert_type""",
    """exa_json_path=$.indicator_name,exa_field_name=alert_name""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.data_source,exa_field_name=alert_source""",            
    """exa_json_path=$.indicator_uuid,exa_field_name=alert_id""",
    """exa_json_path=$.indicator_id,exa_field_name=threat_id""",
    """exa_json_path=$.indicator_category_id,exa_field_name=category_id""",
    """exa_json_path=$.ui_link,exa_field_name=url""",
    """exa_json_path=$.risk_probability,exa_field_name=risk_level""",
    """exa_json_path=$.tenant_id,exa_field_name=tenant_id""",
    """exa_json_path=$.entity_type,exa_field_name=entity_type""",
  ]
  ParserVersion = "v1.0.0"


}
```