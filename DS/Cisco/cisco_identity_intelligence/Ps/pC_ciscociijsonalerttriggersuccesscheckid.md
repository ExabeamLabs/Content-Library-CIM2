#### Parser Content
```Java
{
Name = cisco-cii-json-alert-trigger-success-checkid
  Vendor = Cisco
  Product = Cisco Identity Intelligence
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"checkId":""", """"title":""", """"frameworks":""", """"detail-type":""", """"FAILED_CHECK"""", """"severity":""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.account,exa_field_name=account""",
    """exa_json_path=$.region,exa_field_name=region""",
    """exa_json_path=$.detail.id,exa_field_name=alert_id""",
    """exa_json_path=$.detail.checkId,exa_field_name=alert_type""",
    """exa_json_path=$.detail.title,exa_field_name=alert_name""",
    """exa_json_path=$.detail.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.detail.usersFailing[:1],exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))$""",
    """exa_json_path=$.detail.login,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))$""",
    """exa_json_path=$.detail.frameworks,exa_field_name=more_info""",
    """exa_json_path=$.detail.explainabilityDetails,exa_field_name=additional_info""",
    """exa_json_path=$.detail.description,exa_field_name=additional_info""",
    """exa_json_path=$.detail.explainabilityDetails[?(@.key == 'userTitle')].value,exa_field_name=user_type"""
  ]


}
```