#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-endpoint-notification-success-awscloudtrailinsight
Vendor = Amazon
Product = AWS CloudTrail
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
ParserVersion = v1.0.0
Conditions = [ """"destinationServiceName":"AWS"""", """"dproc":"CloudTrail"""",  """"eventType":"AwsCloudTrailInsight"""" ]
Fields = [
  """exa_json_path=$.eventTime,exa_field_name=time""",
  """exa_json_path=$.destinationServiceName,exa_field_name=app""",
  """exa_json_path=$.insightDetails.eventSource,exa_field_name=src_host""",
  """exa_json_path=$.insightDetails.eventName,exa_field_name=event_name""",
  """exa_json_path=$.eventType,exa_field_name=event_category""",
  """exa_json_path=$.eventID,exa_field_name=alert_id""",
  """exa_json_path=$.awsRegion,exa_field_name=region""",
  """exa_json_path=$.eventCategory,exa_field_name=event_category""",
  """exa_json_path=$.recipientAccountId,exa_field_name=aws_account"""
  ]


}
```