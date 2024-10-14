#### Parser Content
```Java
{
Name = "recordedfuture-ti-kv-app-notification-success-aiinsights"
  Vendor = Recorded Future
  Product = Recorded Future Threat Intelligence
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]
  Conditions = [ """destinationServiceName =Recorded Future""", """"ai_insights""", """"rule""", """"title""" ]
  Fields = [
    """exa_json_path=$.log.triggered,exa_field_name=time""",
    """exa_json_path=$.ai_insights.comment,exa_field_name=additional_info""",
    """exa_json_path=$.rule.name,exa_field_name=rule""",
    """exa_json_path=$.rule.id,exa_field_name=rule_id""",
    """exa_json_path=$.url.portal,exa_field_name=url""",
    """exa_json_path=$.title,exa_field_name=event_name""",
    """exa_json_path=$.type,exa_field_name=category""",
    """"@timestamp\\?":\\?"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"triggered\\?":\\?"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"ai_insights\\?".+?\\?"comment\\?":\\?"({additional_info}[^\\"]+)""",
    """"rule\\?".+?\\?"name\\?":\\?"({rule}[^\\"]+)""",
    """"rule\\?".+?\\?"id\\?":\\?"({rule_id}[^\\"]+)""",
    """"url\\?".+?\\?"portal\\?":\\?"({url}[^\\"]+)""",
    """"title\\?":\\?"({event_name}[^\\"]+)""",
    """"type\\?":\\?"({category}[^\\"]+)""",
  ]
  ParserVersion = "v1.0.0"  


}
```