#### Parser Content
```Java
{
Name = pan-aperture-sk4-alert-trigger-success-policyviolation
    Vendor = Palo Alto Networks
    Product = Palo Alto Aperture
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """"policy_violation"""", """cloud_app_instance""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z""",
      """\Wpolicy_rule_name\s*=\s*"({alert_name}[^"]+)"""",
      """\Witem_type\s*=\s*"({item_type}[^"]+)"""",
      """\Witem_type\s*=\s*"user"(\s*\w+\s*=\s*"[^"]*")*\s*item_name\s*=\s*"(Unknown|({email_address}[^"]+))"""",
      """\Witem_name\s*=\s*"(Unknown|({email_address}[^"]+))"(\s*\w+\s*=\s*"[^"]*")*\s*item_type\s*=\s*"user"""",
      """\Wcloud_app_instance\s*=\s*"({alert_type}[^"]+)"""",
      """\Waction_taken\s*=\s*"({additional_info}[^"]+)"""",
      """"policy_rule_name":"({alert_name}[^"]+)""",
      """"item_type":"({item_type}[^"]+)""",
      """"item_type":"user".*?"item_name":"(Unknown|({email_address}[^"]+))""",
      """"item_name":"(Unknown|({email_address}[^"]+))".*?"item_type":"user"""",
      """"cloud_app_instance":"({alert_type}[^"]+)""",
      """"action_taken":"({additional_info}[^"]+)""",
      """"item_creator":"(|({item_creator}[^"]+))"""",
      """"item_creator_email":"(|Unknown|({email_address}[^"]+))"""",
      """"collaborators":"(|({collaborators}[^"]+))"""",
      """"severity":({alert_severity}[\d.]+)"""
    ]
    SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_type->description", "host->dlpDeviceName"]
    NameTemplate = """Palo Alto DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="user", Name ="windows_id", Fields=["user->windows_id"]

}
```