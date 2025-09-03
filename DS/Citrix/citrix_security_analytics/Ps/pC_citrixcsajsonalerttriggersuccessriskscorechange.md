#### Parser Content
```Java
{
Name = citrix-csa-json-alert-trigger-success-riskscorechange
  Vendor = Citrix
  Product = Citrix Security Analytics
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"cur_riskscore":""", """"event_type":"riskScoreChange"""", """"entity_id":"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.event_type,exa_field_name=event_name""",
    """exa_json_path=$.entity_id,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.alert_type,exa_field_name=alert_type""",
    """exa_json_path=$.alert_message,exa_field_name=alert_name""",
    """exa_json_path=$.alert_value,exa_field_name=alert_severity""",
    """exa_json_path=$.cur_riskscore,exa_field_name=risk_score""",
    """exa_json_path=$.tenant_id,exa_field_name=tenant_id""",
    """exa_json_path=$.entity_type,exa_field_name=entity_type""",
  ]
  ParserVersion = "v1.0.0"  


}
```