#### Parser Content
```Java
{
Name = amazon-awscloudwatch-json-app-notification-success-metricalarm
  Vendor = "Amazon"
  Product = "AWS CloudWatch"
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"alarmType":""", """"MetricAlarm"""", """"historySummary":""", """"historyItemType":""", """"historyData":""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.historyItemType,exa_field_name=operation""",
    """exa_json_path=$.historySummary,exa_field_name=operation_details""",
    """exa_json_path=$.alarmName,exa_field_name=event_name""",
    """exa_json_path=$.alarmType,exa_field_name=event_subtype""",
    """exa_json_path=$.historyData,exa_field_name=additional_info""",
    """exa_json_path=$.historyData,exa_regex=\{.*?newState\\*":\{[^\}]*?\\*"stateValue\\*":\\*"({result}[^"]+?)\\*"""",
    """exa_json_path=$.historyData,exa_regex=\{.*?newState\\*":\{[^\}]*?\\*"stateReason\\*":\\*"({result_reason}[^"]+?)\\*"""",
    """exa_json_path=$.historyData,exa_regex=\{.*?\\*"type\\*":\\*"({action}[^"]+?)\\*"""",
    """exa_json_path=$.historyData,exa_regex=\{.*?\\*"error\\*":\\*"({failure_reason}[^"]+?)\\*"""",
    """exa_json_path=$.historyData,exa_regex=\{.*?\\*"alarmArn\\*":\\*"({role_arn}[^"]+?)\\*""""
  ]


}
```