#### Parser Content
```Java
{
Name = microsoft-sentinel-sk4-alert-trigger-success-loganalytics
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure Sentinel
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  start_timeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ"]
  end_timeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ"]
  processing_end_timeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """"ProductName":"Azure Sentinel"""", """destinationServiceName =Azure""", """dproc=Log Analytics OMS Workspace""" ]
  Fields=[
    """"+AlertName"+:"+({alert_name}[^"]+)""",
    """"+AlertSeverity"+:"+({alert_severity}[^"]+)""",
    """"+SystemAlertId"+:"+({alert_id}[^"]+)""",
    """"+Description"+:"+({additional_info}.+?)\s*"""",
    """"+RemediationSteps"+:"+\[({remediation_steps}[^\]]+)""",
    """"+AlertType"+:"+({alert_type}[^"]+)""",
    """"+TimeGenerated"+:"+({time}[^"]+)""",
    """"+StartTime"+:"+({start_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"+EndTime"+:"+({end_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"IsIncident"+:({is_incident}[^,]+)""",
    """"ProcessingEndTime"+:"+({processing_end_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"Machine Name\\"+:\s*\\"({src_host}[^"]+)\\""",
    """"Process Name\\*"+:\s*\\*"(({process_path}({process_dir}[^.]+)\\({process_name}[^"]+))\\)""",
    """"Command Line\\*"+:\s*\\*"+\\*"+({process_command_line}.*?)\\+"""",
    """"User SID\\*"+:\s*\\*"+({user_sid}.*?)\\"""",
    """"Account Logon Id\\*"+:\s*\\*"+({login_id}[^"]+)\\""",
    """"Account\\":\s*\\"+({domain}[^\\]*?)\\{1,25}({user}[^"]*?)\\",""",
    """"ActionTaken\\":\s*\\"+({action}.*?)\\*"""",
    """"DnsDomain\\":\s*\\"+(\s*|({dns_domain}.*?))\\*"""",
    """"NTDomain\\":\s*\\"+(\s*|({nt_domain}.*?))\\*"""",
    """"IsDomainJoined\\"+:\s*({domain_join}\w+)""",
    """"AlertLink":"({malware_url}[^"]+)""",
    """"HostName\\"+:\s*\\"({host}.*?)\\*"""",
    ]
   SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_type->malwareCategory", "src_host->malwareVictimHost","malware_url->malwareAttackerFile"]
    NameTemplate = """Microsoft azure security Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_host->host_name"]

}
```