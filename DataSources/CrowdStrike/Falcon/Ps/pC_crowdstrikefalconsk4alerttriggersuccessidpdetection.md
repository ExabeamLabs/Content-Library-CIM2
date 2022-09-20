#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-alert-trigger-success-idpdetection
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Conditions = [ """"eventType":"IdpDetectionSummaryEvent"""", """"Severity":""", """"FalconHostLink":"""", """"DetectName":"""", """destinationServiceName =CrowdStrike""" ]
  Fields = [
    """"eventCreationTime":({time}\d{10}),""",
    """"DetectId":"({alert_id}[^"]+)"""",
    """"Severity":({alert_severity}\d{1,5}),""",
    """"DetectName":"({alert_name}[^"]+)"""",
    """"Technique":"({alert_type}[^"]+)"""",
    """"eventType":"({alert_type}[^"]+)"""",
    """"SourceAccountDomain":"({domain}[^"]+)"""",
    """"SourceAccountName":"(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[^"]+))"""",
    """"SourceAccountUpn":"({email_address}[^@"]+@[^\."]+\.[^"]+)"""",
    """"SourceAccountObjectSid":"({user_sid}[^"]+)"""",
    """"SourceEndpointHostName":"({src_host}[^"]+)"""",
    """"SourceEndpointIpAddress":"({src_ip}[a-fA-F\d:\.]+)"""",
    """"TargetEndpointHostName":"({dest_host}[^"]+)"""",
    """"DetectDescription":"({additional_info}[^"]+)"""",
    """"FalconHostLink":"({falcon_host_link}[^"]+)"""",
    """"Tactic":"({category}[^"]+)"""",
  ]


}
```