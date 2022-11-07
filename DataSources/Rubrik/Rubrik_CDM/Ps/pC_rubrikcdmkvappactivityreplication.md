#### Parser Content
```Java
{
Name = rubrik-cdm-kv-app-activity-replication
  Conditions = [
    """ Rubrik [""",
    """clusterName ="""",
    """ eventName ="""",
    """ nodeIpAddress="""
  ]
  ParserVersion = "v1.0.0"

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