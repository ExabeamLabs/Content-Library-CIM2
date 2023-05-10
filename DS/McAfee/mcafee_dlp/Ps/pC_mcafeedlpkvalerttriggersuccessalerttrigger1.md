#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-alerttrigger-1
	ParserVersion = v1.0.0
    Vendor = McAfee
    Product = McAfee DLP
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """, classification""", """, dlpAgentVersion=""", """, incidentId=""", """, policyName =""" ]
    Fields = [
      """\Wclassification="({pci_hits}\S+)\s+\[({phi_hits}.+?)\](\s+\(({pii_hits}\d+)\))?""",
      """\WincidentId="({alert_id}[^"]+)""",
      """\WinsertionTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\WruleNames="({alert_name}[^"]+)""",
      """\Wseverity="({alert_severity}[^"]+)""",
      """\WtotalContentSize="({bytes}\d+)""",
      """\Wdestination="({additional_info}[^"]+)""",
      """\WcomputerName ="({src_host}[^"]+)""",
      """\WipAddress="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\WuserName ="({user}[^"]+)""",
      """\WpolicyName ="({policy_name}[^"]+)""",
      """\WfileName ="({target}[^"]+)""",
      """\WeventType="({alert_type}[^"]+)""",
    ]
    SOAR {
      IncidentType = "dlp"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_type->dlpActionTaken", "src_host->dlpDeviceName"]
      NameTemplate = """McAfee DLP Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```