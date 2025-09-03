#### Parser Content
```Java
{
Name = "google-cloudplatform-json-network-traffic-success-payload"
  ParserVersion = "v1.0.0"
  Vendor = "Google"
  Product = "Google Cloud Platform"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
""""jsonPayload":"""
""""vm_name":"""
""""vpc_name":"""
""""gce_subnetwork""""
  ]
  Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s"""
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""start_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""vpc_name":"(::ffff:)?(default|({host}[^\"]+))"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""src_port":({src_port}\d+)"""
""""protocol":({protocol}\d+)"""
""""dest_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""dest_port":({dest_port}\d+)"""
""""bytes_sent":"({bytes_out}\d+)"""
""""packets_sent":"({packets}\d+)"""
""""dest_instance":\{[^\}]*?\"vm_name\":\"({dest_host}[^\"]+)"""
""""src_instance":\{[^\}]*?\"vm_name\":\"({src_host}[^\"]+)"""
""""reporter":"({reporter}[^\"]+)"""
""""direction":"({direction}[^"]+)""""
"""exa_json_path=$.timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""exa_json_path=$.jsonPayload.start_time,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""exa_regex="start_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""exa_json_path=$.jsonPayload.vpc.vpc_name,exa_field_name=host"""
"""exa_regex="vpc_name":"(::ffff:)?(default|({host}[^\"]+))"""
"""exa_json_path=$.jsonPayload.dest_vpc.vpc_name,exa_field_name=dest_host"""
"""exa_json_path=$.jsonPayload.src_vpc.vpc_name,exa_field_name=src_host"""
"""exa_json_path=$.jsonPayload.connection.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.jsonPayload.connection.src_port,exa_field_name=src_port"""
"""exa_json_path=$.jsonPayload.connection.protocol,exa_field_name=protocol"""
"""exa_json_path=$.jsonPayload.connection.dest_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""exa_json_path=$.jsonPayload.connection.dest_port,exa_field_name=dest_port"""
"""exa_json_path=$.jsonPayload.bytes_sent,exa_field_name=bytes_out"""
"""exa_json_path=$.jsonPayload.packets_sent,exa_field_name=packets"""
"""exa_json_path=$.jsonPayload.reporter,exa_field_name=reporter"""
"""exa_json_path=$.jsonPayload.bytes_sent,exa_field_name=bytes_out"""
"""exa_json_path=$.jsonPayload.rule_details.direction,exa_field_name=direction"""
"""exa_json_path=$.jsonPayload.rule_details.action,exa_field_name=action"""
"""exa_json_path=$.jsonPayload.src_instance.vm_name,exa_field_name=src_host"""
"""exa_json_path=$.jsonPayload.dest_instance.vm_name,exa_field_name=dest_host"""
  ]


}
```