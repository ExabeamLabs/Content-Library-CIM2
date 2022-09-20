#### Parser Content
```Java
{
Name = symantec-cloudsoc-sk4-alert-trigger-success-fromdetect
  Vendor = Symantec
  Product = Symantec CloudSOC
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""destinationServiceName =Symantec CloudSOC""" , """dproc=Detect App""", """"from_detect""""]
  Fields = [
    """"inserted_timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""""
    """suser=({email_address}[^\s]+@.+?)\s\w+=""",
    """"user_name":"({full_name}[^"]+)""",
    """"user":"({email_address}[^\@]+@[^"]+)""",
    """"user":"({user}[^\@"]+)"""",
    """"service":"({process_path}[^"]+)"""",
    """"browsers":\["({browser}[^"]+)"""",
    """"user_agent":"({user_agent}[^"]+)"""",
    """"activity_type":"({operation}[^"]+)"""",
    """"ioi_code":"({alert_type}[^"]+)"""",
    """"message":"({alert_name}[^"]+)"""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"object_type":"({object_type}[^"]+)"""",
    """"object_name":"(|\/|({object}({file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({file_name}[^\\\/=]*?(\.({file_ext}[^"]+))?)?))))"""",
    """"name":"(|\/|({object}({file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({file_name}[^\\\/=]*?(\.({file_ext}[^"]+))?)?))))""""
    """"host(s)?":"({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""",
  ]
  DupFields = ["file_path->resource"]
  ParserVersion = "v1.0.0"


}
```