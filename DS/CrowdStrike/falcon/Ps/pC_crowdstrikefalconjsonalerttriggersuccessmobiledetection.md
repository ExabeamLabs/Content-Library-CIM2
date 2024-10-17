#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-alert-trigger-success-mobiledetection
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = v1.0.0
  TimeFormat = ["epoch", "epoch_sec"]
  Conditions = [ """"eventType":"MobileDetectionSummaryEvent"""", """"MobileDetectionId":""", """"FalconHostLink":""" ]
  Fields = [
    """"eventCreationTime":({time}\d{10,13})""",
    """"eventType":"({event_name}[^"]+)"""",
    """"DetectName":"({alert_type}[^"]+)"""",
    """"Technique":"({alert_name}[^"]+)"""",
    """"Severity":({alert_severity}[^",]+)""", 
    """"DetectDescription":"({additional_info}[^"]+?)\.?"""",
    """"FalconHostLink":"({falcon_host_link}[^"]+)"""",
    """"ComputerName":"({src_host}[\w-.]+)"""",
    """"UserName":"*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))($|"|<)"""
    
  ]


}
```