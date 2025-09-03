#### Parser Content
```Java
{
Name = google-cloudplatform-json-scheduled-success-scheduler
  Vendor = Google
  Product = Google Cloud Platform
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"type":"cloud_scheduler_job"""","""google.cloud.scheduler.logging"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"service_name":"({service_name}[^"]+)"""",
    """destinationServiceName =({app}[^=]+?)\s\w+=""",
	  """"@type":".+?({event_name}scheduler[^"]+)"""",
    """"jobName":"({object}[^"]+)"""",
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$..timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """exa_json_path=$.logName,exa_field_name=log_name"""
    """exa_json_path=$..location,exa_field_name=region"""
    """exa_json_path=$..project_id,exa_field_name=project_id"""
    """exa_json_path=$.jsonPayload.jobName,exa_field_name=object"""
    """exa_json_path=$.resource.type,exa_field_name=category"""
    """exa_regex=@type":".+?({event_name}scheduler[^"]+)"""",
  ]
  ParserVersion = v1.0.0


}
```