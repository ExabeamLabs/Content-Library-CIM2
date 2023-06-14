#### Parser Content
```Java
{
Name = pan-aperture-sk4-alert-trigger-success-incident
    Vendor = Palo Alto Networks
    Product = Palo Alto Aperture
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"incident"""", """"cloud_app_instance"""", """"item_owner":""", """"item_creator_email":""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z""",
      """\Wpolicy_rule_name\s*=\s*"({alert_name}[^"]+)"""",
      """\Witem_type\s*=\s*"({item_type}[^"]+)"""",
      """\Witem_name\s*=\s*"({item_name}[^"]+?)\s*"""",
      """\Witem_owner\s*=\s*"({first_name}[^",\s]+)\s+({last_name}[^",\s]+)"""",
      """\Witem_owner\s*=\s*"({last_name}[^",\s]+)\s*\,\s*({first_name}[^",\s]+)"""",
      """\Witem_owner\s*=\s*"({user}[^",\s@]+)"""",
      """\Wcloud_app_instance\s*=\s*"({alert_type}[^"]+)"""",
      """"policy_rule_name":"({alert_name}[^"]+)""",
      """"item_type":"({item_type}[^"]+)""",
      """"item_name":"({item_name}[^"]+?)\s*"""",
      """"item_owner":"({first_name}[^",\s]+)\s+({last_name}[^",\s]+)"""",
      """"item_owner":"({user}[^",\s@]+)"""",
      """"cloud_app_instance":"({alert_type}[^"]+)""",
      """"item_creator":"(|({item_creator}[^"]+))"""",
      """"item_creator_email":"(|({email_address}[^\s",@]+\@[\w\.\-]+))"""",
      """"collaborators":"(|({collaborators}[^"]+))"""",
      """"severity":({alert_severity}[\d.]+)""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    ]
    SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpFileOwner", "item_name->dlpFileName", "alert_name->dlpPolicy", "host->dlpDeviceName", "alert_type->description"]
    NameTemplate = """Palo Alto DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="user", Name ="windows_id", Fields=["user->windows_id"]

}
```