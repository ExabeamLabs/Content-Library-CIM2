#### Parser Content
```Java
{
Name = vmware-carbonblackedr-sk4-process-create-success-redcanary
  Vendor = VMware
  Product = Carbon Black EDR 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """event_type_cd""", """sensor_product_cd":"cb_response"""", """requestClientApplication=RedCanary""", """destinationServiceName =Custom Application""", """process_path""" ]
  Fields =[
    """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",
    """"sensor_id"+:"+({sensor_id}[^"]+)""",
    """"+process_path"+:"+({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+))""",
    """"host_name"+:"+({host}[^"]+)""",
    """"process_command_line"+:"+({process_command_line}[^"]+)"*,""",
    """"process_md5"+:"+({hash_md5}[^"]+)"*,""",
    """"user_username"+:"+({user}[\w\.\-]{1,40}\$?)"*,""",
    """"user_domain"+:"+({domain}[^"]+)"*,"""
    ]
    DupFields = ["host->dest_host"]
    ParserVersion = "v1.0.0"


}
```