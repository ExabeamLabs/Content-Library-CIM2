#### Parser Content
```Java
{
Name = pan-prisma-json-alert-trigger-success-catchall
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = Prisma Cloud
  ExtractionType = json
  TimeFormat = """MMM dd, yyyy HH:mm:ss Z"""
  Conditions = [ """"type":""", """"containerID":""", """"rule":""", """tags""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.type,exa_field_name=alert_type""",
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.rule,exa_field_name=rule""",
    """exa_json_path=$.message,exa_field_name=additional_info""",
    """exa_json_path=$.containerID,exa_field_name=container_id""",
    """exa_json_path=$.category,exa_field_name=alert_name""",
    """exa_json_path=$.aggregatedAlerts,exa_field_name=more_info""",
    """exa_json_path=$.osRelease,exa_field_name=os""",
    """exa_json_path=$.accountIDs[:1],exa_field_name=account_id"""
  ]


}
```