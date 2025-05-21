#### Parser Content
```Java
{
Name = amazon-awscloudwatch-kv-app-notification-success-metricalarm
  Vendor = "Amazon"
  Product = "AWS CloudWatch"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """AlarmType=MetricAlarm""", """HistoryItemType=""", """HistorySummary=""", """HistoryData= {""", """AlarmName =""" ]
  Fields = [
    """Timestamp=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z),""",
    """HistoryItemType=({operation}[^,=]+?),\s\w+=""",
    """HistorySummary=({operation_details}[^,=]+?),\s\w+=""",
    """AlarmName =({event_name}[^,=]+?),\s\w+=""",
    """AlarmType=({event_subtype}[^,=]+?),\s\w+=""",
    """HistoryData=\{({additional_info}[^$]+)\}\)?$""",
    """HistoryData=\{.*?newState":\{[^\}]*?"stateValue":"({result}[^"]+)"""",
    """HistoryData=\{.*?newState":\{[^\}]*?"stateReason":"({result_reason}[^"]+)"""",
    """HistoryData=\{.*?"type":"({action}[^"]+?)"""",
    """HistoryData=\{.*?"error":"({failure_reason}[^"]+?)"""",
    """HistoryData=\{.*?"alarmArn":"({role_arn}[^"]+?)""""
  ]


}
```