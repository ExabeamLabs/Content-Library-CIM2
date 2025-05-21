#### Parser Content
```Java
{
Name = rubrik-cdm-kv-app-logout-audit
  ParserVersion = "v1.0.0"
  Conditions = [ """eventType="Audit"""", """ logged out """, """ Rubrik [""", """clusterName ="""", """ eventName ="""", """ nodeIpAddress="""  ]
  Fields = ${DLRubrikParsersTemplates.rubrik-system-info.Fields}[
    """tracerId="\S+\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)[^=]+logged out"""
  ]

rubrik-system-info = {
    Vendor = Rubrik
    Product = Rubrik Cloud Data Management
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """nodeId="({host}[^"]+)"""",
      """nodeIpAddress="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
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