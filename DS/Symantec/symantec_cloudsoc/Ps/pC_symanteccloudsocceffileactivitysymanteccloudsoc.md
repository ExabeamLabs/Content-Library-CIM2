#### Parser Content
```Java
{
Name = "symantec-cloudsoc-cef-file-activity-symanteccloudsoc"
Vendor = "Symantec"
Product = "Symantec CloudSOC"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""destinationServiceName =Symantec CloudSOC"""
]
Fields = [
""""inserted_timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""""
"""suser=({email_address}[^\s]+@.+?)\s\w+="""
""""user_name":"({full_name}[^"]+)"""
""""user":"({email_address}[^\@]+@({email_domain}[^"]+))"""
""""user":"(system|({email_address}[^\@]+@[^"]+))"""
""""service":"({app}[^"]+)""""
""""browsers":(\[)?"({browser}[^"]+)""""
""""user_agent":"({user_agent}[^"]+)""""
""""activity_type":"({operation}[^"]+)""""
""""ioi_code":"({alert_type}[^"]+)""""
""""message":"({additional_info}[^"]+)""""
""""severity":"({alert_severity}[^"]+)""""
""""object_type":"({object_type}[^"]+)""""
""""object_name":"(|\/|({object}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?))))""""
""""name":"(|\/|({object}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?))))""""
""""host(s)?":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""shared_with":"({target}[^"]+)""""
]
DupFields = [
"src_file_path->resource"
"app->service_name"
"operation->access"
]
ParserVersion = "v1.0.0"


}
```