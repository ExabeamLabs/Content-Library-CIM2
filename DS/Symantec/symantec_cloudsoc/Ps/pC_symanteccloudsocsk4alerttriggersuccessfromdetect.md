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
    """"user":"({user}[\w\.\-]{1,40}\$?)"""",
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
    """"host(s)?":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  ]
  DupFields = ["file_path->resource"]
  ParserVersion = "v1.0.0"


}
```