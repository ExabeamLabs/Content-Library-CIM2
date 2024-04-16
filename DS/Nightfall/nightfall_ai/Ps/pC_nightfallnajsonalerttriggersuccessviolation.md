#### Parser Content
```Java
{
Name = nightfall-na-json-alert-trigger-success-violation
  Vendor = Nightfall
  Product = Nightfall AI
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """"violationLink"""", """nightfall.ai""", """fileName""", """violationTime""", """"eventType":"violation"""" ]
  Fields = [
    """exa_json_path=$.violationTime,exa_field_name=time""",
    """exa_json_path=$..detector.name,exa_field_name=alert_name""",
    """exa_json_path=$.who.email,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))""",
    """exa_json_path=$.who.username,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
    """exa_json_path=$.service,exa_field_name=alert_source""",
    """exa_json_path=$.foundIn,exa_field_name=operation""",
    """exa_json_path=$.eventType,exa_field_name=alert_type""",
    """exa_json_path=$.detectionRule.name,exa_field_name=rule""",
    """exa_json_path=$.policy.name,exa_field_name=policy_name""",
    """exa_json_path=$.fileName,exa_regex=({file_path}(?:({file_dir}[^"]+)[\/]+)?)?({file_name}[^"\/]+?(\.({file_ext}[^"\.]+))?)""",
    """exa_json_path=$.violationLink,exa_field_name=url""",
    """exa_json_path=$.permalink,exa_field_name=additional_info""",
  ]


}
```