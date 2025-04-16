#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-notification-success-fdritemsexplorer
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Conditions = [ """destinationServiceName =CrowdStrike""", """dproc=FDR Items explorer""", """"event-type":""" ]
  Fields = [
    """exa_json_path=$..event-type,exa_field_name=event_name""",
    """exa_json_path=$..cid,exa_field_name=cid""",
    """exa_json_path=$..service,exa_field_name=service_name""",
    """exa_json_path=$..disposition,exa_field_name=disposition""",
    """exa_json_path=$..scan_id,exa_field_name=scan_id""",
    """exa_json_path=$..resource,exa_field_name=resource""",
    """exa_json_path=$..aws_account_id,exa_field_name=account_id""",
    """exa_json_path=$..azure_tenant_id,exa_field_name=tenant_id""",
    """exa_json_path=$..AttackTypes,exa_field_name=attack_info""",
    """exa_json_path=$..azure_resource_id,exa_field_name=resource_id""",
    """exa_json_path=$..azure_subscription_id,exa_field_name=subscription_id"""
  ]
  ParserVersion = "v1.0.0"


}
```