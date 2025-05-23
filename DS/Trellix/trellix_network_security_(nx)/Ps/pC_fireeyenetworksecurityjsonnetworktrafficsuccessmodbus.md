#### Parser Content
```Java
{
Name = "fireeye-networksecurity-json-network-traffic-success-modbus"
	Conditions = [ """"event_type":"modbus"""", """"flow_id":""", """"modbus":{""", """"transaction_id":""", """"function_code":"""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
  	  """exa_json_path=$.modbus.transaction_id,exa_field_name=server_ssh_version""",
  	  """exa_json_path=$.modbus.function_code,exa_field_name=operation""",
  	  """exa_json_path=$.modbus.function_category,exa_field_name=category""",
    ]
	ParserVersion = "v1.0.0"

fireeye-networksecurity-nx-events = {
  Vendor = Trellix
  Product = Trellix Network Security (NX)
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.iface,exa_field_name=interface_name""",
    """exa_json_path=$.session_key,exa_field_name=session_id""",
    """exa_json_path=$.event_type,exa_field_name=event_category""",
    """exa_json_path=$.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)""",
    """exa_json_path=$.src_port,exa_field_name=src_port""",
    """exa_json_path=$.dest_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)""",
    """exa_json_path=$.dest_port,exa_field_name=dest_port""",
    """exa_json_path=$.proto,exa_field_name=protocol""",
    """exa_json_path=$.app_proto,exa_field_name=app_protocol"""
  
}
```