#### Parser Content
```Java
{
Name = rubrik-cdm-kv-app-login-success-loggedin
    Vendor = Rubrik
    Product = Rubrik Cloud Data Management
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ParserVersion = "v1.0.0"
    Conditions = [ """eventType="Audit"""", """ logged in from """, """ Rubrik [""", """clusterName ="""", """ eventName ="""", """ nodeIpAddress="""  ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """nodeId="({host}[^"]+)"""",
      """nodeIpAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
	   """eventName ="({event_name}[^"]+)"""",
      """status="({result}[^"]+)"""",
      """objectName ="(-|({object}[^"]+))"""",
      """objectType="({object_type}[^"]+)"""",
      """objectId="({object_id}[^"]+)"""",
      """eventSeverity="({alert_severity}[^"]+)"""",
      """\]\s+({user}[^(]+)\s(\([^\)]+\)\s)*in '[^\']+' logged in from""",
      """\(({user_ou}[^)]+)\) in '[^\']+' logged in from""",
      """logged in from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""                          
    ]
    DupFields = [ "host->dest_host"]
  

}
```