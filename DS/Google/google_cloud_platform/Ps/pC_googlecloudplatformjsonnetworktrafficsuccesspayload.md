#### Parser Content
```Java
{
Name = "google-cloudplatform-json-network-traffic-success-payload"
  ParserVersion = "v1.0.0"
  Vendor = "Google"
  Product = "Google Cloud Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
""""jsonPayload":"""
""""vm_name":"""
""""vpc_name":"""
""""gce_subnetwork""""
  ]
  Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s"""
"""\"start_time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\"vpc_name\":\"(::ffff:)?(default|({host}[^\"]+))"""
"""\"src_ip\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"src_port\":({src_port}\d+)"""
"""\"protocol\":({protocol}\d+)"""
"""\"dest_ip\":\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\"dest_port\":({dest_port}\d+)"""
"""\"bytes_sent\":\"({bytes_out}\d+)"""
"""\"packets_sent\":\"({packets}\d+)"""
"""\"dest_instance\":\{[^\}]*?\"vm_name\":\"({dest_host}[^\"]+)"""
"""\"src_instance\":\{[^\}]*?\"vm_name\":\"({src_host}[^\"]+)"""
"""\"reporter\":\"({reporter}[^\"]+)"""
  ]


}
```