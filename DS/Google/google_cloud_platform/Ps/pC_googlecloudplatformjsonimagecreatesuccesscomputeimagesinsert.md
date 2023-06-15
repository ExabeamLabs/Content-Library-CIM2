#### Parser Content
```Java
{
Name = google-cloudplatform-json-image-create-success-computeimagesinsert
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  ParserVersion = "v1.0.0"
  Conditions = [ """googleapis.com""", """"methodName":""", """compute.images.insert"""" ]
  Fields = ${GcpParserTemplates.gcp-cloudaudit-json.Fields}[
    """"source({source_resource_type}Snapshot)":\s*"({source_resource}[^"\\]*)"""",
    """"source":\s*"({source_resource}[^"\\]*)"""",
    """"source({source_resource_type}Disk)":\s*"({source_resource}[^"\\]*)"""",
  ]

gcp-cloudaudit-json = {
    Vendor = Google
    Product = Google Cloud Platform
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"logName"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
      """"log-name"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
      """"status":.+"code":\s*({result_code}\d+)""",
      """"status":.+"message":\s*({failure_reason}[^\\},]+)""",
      """"principalEmail":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\s@"]+))"""",
      """"callerIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"callerSuppliedUserAgent":\s*"({user_agent}[^"]+)""",
      """"methodName":\s*"({operation}[^"]+)""",
      """"resourceName":\s*"({resource}({resource_path}[^"]+)\/({resource_name}[^"\/]+))"""",
      """"serviceName":\s*"({service_name}[^"]+)""",
      """"resource":\s*\{\s*"type":\s*"({resource_type}[^"\\\/]+)"""",
      """"resource"+:[^\}]*labels[^\}]*"+project_id"+:\s*"+({project_id}[^"\\\/\}]+)"+""",
      """"resource"+:[^\}]*labels[^\}]*"+zone"+:\s*"+({zone}[^"\\\/\}]+)"+""",
      """"resource"+:[^\}]*labels[^\}]*"+location"+:\s*"+({region}[^"\\\/\}]+)"+""",
      """"resource"+:[^\}]*labels[^\}]*"+bucket_name"+:\s*"+({bucket_name}[^"\\\/\}]+)"+""",
      """"operation"+:[^\}]*first"+:\s*({operation_first}[^"\\\/\}\s,]+)""",
      """"operation"+:[^\}]*last"+:\s*({operation_last}[^"\\\/\}\s,]+)""",
    
}
```