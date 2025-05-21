#### Parser Content
```Java
{
Name = mcafee-es-kv-alert-trigger-success-parametervalue
    Vendor = Trellix
    Product = Trellix Endpoint Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ "signature_name=", "dvc_ip_long=", "parameter_value=" ]
    Fields = [
      """dvc_time="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """dvc_ip_long="({host_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """dvc_host="({host}.+?)",""",
      """source_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """event_id="({alert_id}\d+)""",
      """signature_name="({alert_name}.+?)",""",
      """category="({alert_type}.+?)",""",
      """signature_id="({signature_id}\d+)""",
      """severity="({alert_severity}\d+)""",
      """parameter_name="({additional_info}[^"]+)""",
      """user="(({domain}[^\\]+)\\+)?(?: |({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    ]
    SOAR {
        IncidentType = "malware"
        DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_id->sourceId", "alert_name->malwareName", "alert_type->malwareCategory", "alert_severity->sourceSeverity", "src_ip->malwareVictimHost"]
        NameTemplate = """McAfee EPO Alert ${alert_name} found"""
        ProjectName = "SOC"
        EntityFields = [
          {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address"]

}
```