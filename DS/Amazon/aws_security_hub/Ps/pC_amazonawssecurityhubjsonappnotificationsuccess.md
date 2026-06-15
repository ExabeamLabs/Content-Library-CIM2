#### Parser Content
```Java
{
Name = amazon-awssecurityhub-json-app-notification-success
  Vendor = "Amazon"
  Product = "AWS Security Hub"
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"Compliance":""", """"aws.securityhub"""", """"findings":""", """"detailType":""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.detail.findings[*].Title,exa_field_name=additional_info""",
    """exa_json_path=$.detail.findings[*].AwsAccountId,exa_field_name=account_id""",
    """exa_json_path=$.detail.findings[*].Region,exa_field_name=region""",
    """exa_json_path=$.detail.findings[*].Compliance.Status,exa_field_name=state""",
    """exa_json_path=$.detail.findings[*].Resources[*].Type,exa_field_name=resource_type""",
    """exa_json_path=$.detail.findings[*].FindingProviderFields.Severity.Label,exa_field_name=severity""",
    """exa_json_path=$.detail.findings[*].Description,exa_field_name=more_info""",
    """exa_json_path=$.detail.findings[*].ProductArn,exa_field_name=resource_name""",
    """exa_json_path=$.account,exa_field_name=aws_account""",
    """exa_json_path=$.detail.findings[*].Id,exa_field_name=resource_id"""
    """exa_json_path=$.detail.findings[*].Compliance.StatusReasons[*].Description,exa_field_name=result_reason"""
    """exa_json_path=$.detail.findings[*].Compliance.StatusReasons[*].ReasonCode,exa_field_name=result_code"""
    """exa_json_path=$.detail.findings[*].ProductFields.RecommendationUrl,exa_field_name=url"""
  ]


}
```