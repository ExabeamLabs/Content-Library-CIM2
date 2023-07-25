#### Parser Content
```Java
{
Name = google-cloudplatform-mix-app-activity-success-prototpayload
  Vendor = Google
  Product = Google Cloud Platform
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"protoPayload":""", """googleapis.com""", """"resourceName":""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s""",
    """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"callerIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"serviceName":"({service_name}[^"]+)"""",
    """"callerSuppliedUserAgent":\s*"({user_agent}[^"]+)""",
    """"principalEmail":\s*"(?:({email_address}[^"@]+?@({email_domain}[^"@]+))|({user}[^":]+))"""",
    """"methodName":\s*"({operation}[^"]+)""",
    """"serviceName":\s*"({app}[^"]+)""",
    """\sdproc=({app}[^=]+)\s\w+=""",
    """"bucket_name":"({bucket_name}[^",}]+)""""
    """"resource":\s*\{\s*"type":\s*"({resource_type}[^"\\\/]+)"""",
    """"resourceName":\s*"({resource}({resource_path}[^"]+)\/({resource_name}[^"\/]+))"""",
    """"resource"+:[^\}]*labels[^\}]*"+location"+:\s*"+({region}[^"\\\/\}]+)"+""",
    """"operation"+:[^\}]*first"+:\s*({operation_first}[^"\\\/\}\s,]+)""",
    """"operation"+:[^\}]*last"+:\s*({operation_last}[^"\\\/\}\s,]+)""",
    """"logName"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"log-name"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"resource"+:[^\}]*labels[^\}]*"+project_id"+:\s*"+({project_id}[^"\\\/\}]+)"+"""
    """"status":.+"code":\s*({result_code}\d+)""",
    """"status":.+"message":\s*"?({failure_reason}[^

}
```