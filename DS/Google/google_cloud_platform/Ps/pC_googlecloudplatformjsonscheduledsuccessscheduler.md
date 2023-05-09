#### Parser Content
```Java
{
Name = google-cloudplatform-json-scheduled-success-scheduler
  Vendor = Google
  Product = Google Cloud Platform
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"type":"cloud_scheduler_job"""","""dproc=Cloud PubSub"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"service_name":"({service_name}[^"]+)"""",
    """destinationServiceName =({app}[^=]+?)\s\w+=""",
	  """"@type":".+?({event_name}scheduler[^"]+)"""",
    """"jobName":"({object}[^"]+)"""",
  ]
  ParserVersion = v1.0.0


}
```