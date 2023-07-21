#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-app-activity-success-createlogstream
Vendor = Amazon
Product = AWS CloudTrail
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
ParserVersion = v1.0.0
Conditions = [ """"destinationServiceName":"AWS"""", """"dproc":"CloudTrail"""", """"eventName":"CreateLogStream"""", """"eventType":"AwsCloudTrailInsight"""" ]
Fields = [
  """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ?))"+\s*[,\]\}]""",
  """"destinationServiceName":"({app}[^"]+)"""",
  """"eventSource":"(\s*|({src_host}[^"]+))"""",
  """"eventName":"({event_name}[^"]+)"""",
  """"eventType":"({event_category}[^"]+)"""",
  """"eventID":"({alert_id}[^"]+)""",
  """"awsRegion"\s*:\s*"({region}[^"]+)"""",
  """"eventCategory":\s*"({event_category}[^"]+)""""
  ]


}
```