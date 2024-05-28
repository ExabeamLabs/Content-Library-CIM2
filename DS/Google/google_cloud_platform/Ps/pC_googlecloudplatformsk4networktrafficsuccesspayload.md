#### Parser Content
```Java
{
Name = google-cloudplatform-sk4-network-traffic-success-payload
  ParserVersion = "v1.0.0"
  Vendor = "Google"
  Product = "Google Cloud Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """"jsonPayload":""", """"insertId":""", """googleapis.com""", """"gce_subnetwork"""" ]
  Fields = [
"""\d\d:\d\d:\d\d\.\d+Z?\s(::ffff:)?({host}[\w\-.]+)\s"""
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)"""
""""start_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""src_port":({src_port}\d+)"""
""""protocol":({protocol}\d+)"""
""""dest_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""dest_port":({dest_port}\d+)"""
""""bytes_sent":"({bytes_out}\d+)"""
""""packets_sent":"({packets}\d+)"""
""""reporter":"({reporter}[^\"]+)"""
""""direction":"({direction}[^"]+)""""
"""suser=((?i)anonymous|({user}[\w\.\-]{1,40}\$?))\s+[\w=]+"""
  ]


}
```