#### Parser Content
```Java
{
Name = rubrik-cdm-kv-app-logout-audit
  ParserVersion = "v1.0.0"
  Conditions = [ """eventType="Audit"""", """ logged out """, """ Rubrik [""", """clusterName ="""", """ eventName ="""", """ nodeIpAddress="""  ]
  Fields = ${DLRubrikParsersTemplates.rubrik-system-info.Fields}[
    """tracerId="\S+\s({user}[^\s]+)[^=]+logged out"""
  ]

rubrik-system-info = {
    Vendor = Rubrik
    Product = Rubrik CDM
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """nodeId="({host}[^"]+)"""",
      """nodeIpAddress="({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
      """eventName ="({event_name}[^"]+)"""",
      """status="({result}[^"]+)"""",
      """objectName ="(-|({object}[^"]+))"""",
      """objectType="({object_type}[^"]+)"""",
      """objectId="({object_id}[^"]+)"""",
      """eventSeverity="({alert_severity}[^"]+)"""",
    ]
    DupFields = [ "host->dest_host"
}
```