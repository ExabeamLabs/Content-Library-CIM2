#### Parser Content
```Java
{
Name = google-cloudplatform-json-scheduled-success-scheduler
  Vendor = Google
  Product = Google Cloud Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSZ"
  Conditions = [ """"type":"cloud_scheduler_job"""","""google.cloud.scheduler.logging"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """"service_name":"({service_name}[^"]+)"""",
    """destinationServiceName =({app}[^=]+?)\s\w+=""",
	  """"@type":".+?({event_name}scheduler[^"]+)"""",
    """"jobName":"({object}[^"]+)"""",
  ]
  ParserVersion = v1.0.0


}
```