#### Parser Content
```Java
{
Name = pan-aperture-sk4-alert-trigger-success-policyviolation
    Vendor = Palo Alto Networks
    Product = Palo Alto Aperture
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"policy_violation"""", """cloud_app_instance""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z""",
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)"""
      """\Wpolicy_rule_name\s*=\s*"({alert_name}[^"]+)"""",
      """\Witem_type\s*=\s*"({item_type}[^"]+)"""",
      """\Witem_type\s*=\s*"user"(\s*\w+\s*=\s*"[^"]*")*\s*item_name\s*=\s*"(Unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
      """\Witem_name\s*=\s*"(Unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"(\s*\w+\s*=\s*"[^"]*")*\s*item_type\s*=\s*"user"""",
      """\Wcloud_app_instance\s*=\s*"({alert_type}[^"]+)"""",
      """\Waction_taken\s*=\s*"({additional_info}[^"]+)"""",
      """"policy_rule_name":"({alert_name}[^"]+)""",
      """"item_type":"({item_type}[^"]+)""",
      """"item_type":"user".*?"item_name":"(Unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""",
      """"item_name":"(Unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))".*?"item_type":"user"""",
      """"cloud_app_instance":"({alert_type}[^"]+)""",
      """"action_taken":"({additional_info}[^"]+)""",
      """"item_creator":"(|({item_creator}[^"]+))"""",
      """"item_creator_email":"(|Unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
      """"collaborators":"(|({collaborators}[^"]+))"""",
      """"severity":({alert_severity}[\d.]+)""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    ]
    SOAR {
    IncidentType = "dlp"
    NameTemplate = """Palo Alto DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="user", Name ="windows_id", Fields=["user->windows_id"]

}
```