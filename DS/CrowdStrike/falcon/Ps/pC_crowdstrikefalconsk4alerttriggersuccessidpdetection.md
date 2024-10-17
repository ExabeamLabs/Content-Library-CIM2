#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-alert-trigger-success-idpdetection
  ParserVersion = "v1.0.0"
  Conditions = [ """"eventType":"IdpDetectionSummaryEvent"""", """"Severity":""", """"FalconHostLink":"""", """"DetectName":"""", """destinationServiceName =CrowdStrike""" ]
  
json-crowdstrike-alert = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = ["epoch","epoch_sec"]
  Fields = [
    """"eventCreationTime":({time}\d{10,13}),""",
    """"DetectId":"({alert_id}[^"]+)"""",
    """"Severity":\s*({severity}\d{1,5}),""",
    """"SeverityName":\s*"({alert_severity}[^,"]+)""",
    """"DetectName":"({alert_name}[^"]+)"""",
    """"Technique":"({alert_type}[^"]+)"""",
    """"eventType":"({alert_type}[^"]+)"""",
    """"SourceAccountDomain":"({domain}[^"]+)"""",
    """"SourceAccountName":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"SourceAccountUpn":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"SourceAccountObjectSid":"({user_sid}[^"]+)"""",
    """"SourceEndpointHostName":"({src_host}[^"]+)"""",
    """"SourceEndpointIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"TargetEndpointHostName":"({dest_host}[^"]+)"""",
    """"DetectDescription":"({additional_info}[^"]+)"""",
    """"FalconHostLink":"({falcon_host_link}[^"]+)"""",
    """"Tactic":"({category}[^"]+)"""",
    """"aid":"({aid}[^"]+)"""
    """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
    """exa_regex="eventCreationTime":({time}\d{13})"""
	  """exa_json_path=$.event.DetectId,exa_field_name=alert_id""",
	  """exa_json_path=$.event.Severity,exa_field_name=severity""",
	  """exa_json_path=$.event.SeverityName,exa_field_name=alert_severity""",
	  """exa_json_path=$.event.DetectName,exa_field_name=alert_name""",
	  """exa_json_path=$.event.Technique,exa_field_name=alert_type""",
	  """exa_json_path=$.metadata.eventType,exa_field_name=alert_type""",
	  """exa_json_path=$.event.SourceAccountDomain,exa_field_name=domain""",
	  """exa_json_path=$.event.SourceAccountName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
	  """exa_json_path=$.event.SourceAccountUpn,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
	  """exa_json_path=$.event.SourceAccountObjectSid,exa_field_name=user_sid""",
	  """exa_json_path=$.event.SourceEndpointHostName,exa_field_name=src_host""",
	  """exa_json_path=$.event.SourceEndpointIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
	  """exa_json_path=$.event.TargetEndpointHostName,exa_field_name=dest_host""",
	  """exa_json_path=$.event.DetectDescription,exa_field_name=additional_info""",
	  """exa_json_path=$.event.FalconHostLink,exa_field_name=falcon_host_link""",
	  """exa_json_path=$.event.Tactic,exa_field_name=category""",
	  """exa_json_path=$.event.aid,exa_field_name=aid"""
  
}
```