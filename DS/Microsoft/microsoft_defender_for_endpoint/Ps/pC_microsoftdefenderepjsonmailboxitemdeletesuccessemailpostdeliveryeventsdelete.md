#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-mailbox-item-delete-success-emailpostdeliveryeventsdelete"
  Vendor = Microsoft
  Product = "Microsoft Defender for Endpoint"
  Conditions = [ """"category":""", """"AdvancedHunting-EmailPostDeliveryEvents"""", """"ActionType":""", """"Manual Remediation"""", """"DeliveryLocation":"Delete"""" ]
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ssZ" ]
  Fields = [
    """exa_json_path=$..Timestamp,exa_field_name=time""",
    """exa_json_path=$..Action,exa_field_name=action""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$..DetectionMethods,exa_field_name=additional_info""",
    """exa_json_path=$..ActionType,exa_field_name=event_name""",
    """exa_json_path=$..ActionResult,exa_field_name=result""",
    """exa_json_path=$..RecipientEmailAddress,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$..NetworkMessageId,exa_field_name=message_id"""
  ]
ParserVersion = "v1.0.0"


}
```