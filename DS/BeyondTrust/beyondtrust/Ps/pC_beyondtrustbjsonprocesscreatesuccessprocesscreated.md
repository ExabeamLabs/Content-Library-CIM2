#### Parser Content
```Java
{
Name = beyondtrust-b-json-process-create-success-processcreated
  Vendor = BeyondTrust
  Product = BeyondTrust
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"process_name":"""",""""vendor_product":"Beyondtrust Privilege Management"""", """"process_start_time":"""" ]
  Fields = [
  """"process_start_time":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,3}Z)"""
  """"process_id":"?({process_id}\d+)"""
  """process_path":"({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+))""""
  """"process":"({process_command_line}[^,]+)",""""
  """"action":"({action}[^"]+)""""
  """"user":"({user}[\w\.\-]{1,40}\$?)""""
  """"dest":"({dest_host}[\w\-\.]+)"""
  """"user_id":"({user_sid}S-[^"]+)"""
  """"description":"({additional_info}[^"]+)"""
  """"parent_process":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))""""
  """"parent_process_id":"?({parent_process_id}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```