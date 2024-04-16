#### Parser Content
```Java
{
Name = rubrik-cdm-kv-user-create-success-createlocaluser
    ParserVersion = v1.0.0
    Conditions = [ """ Rubrik """, """status="Success"""", """eventName ="Audit.CreateLocalUserAudit"""", """ created local user """ ]
    Fields = ${RubrikCDMParserTemplates.rubrik-events.Fields}[
      """\] ({user}[\w\.\-]{1,40}\$?) [^\)]+?\) created local user '({account_name}[^']+?)'"""
   ],
   DupFields = ${RubrikCDMParserTemplates.rubrik-events.DupFields}["account_name->dest_user"]
  
rubrik-events = {
  Vendor = Rubrik
  Product = Rubrik Cloud Data Management
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """nodeId="({host}[^"]+)"""",
      """nodeIpAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """eventName ="({event_code}[^"]+)"""",
      """status="({result}[^"]+)"""",
      """objectName ="(-|({object}[^"]+))"""",
      """objectType="({object_type}[^"]+)"""",
      """objectId="({object_id}[^"]+)"""",
      """eventSeverity="({alert_severity}[^"]+)"""",
  ]
  DupFields = [ "host->dest_host"
}
```