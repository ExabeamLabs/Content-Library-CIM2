#### Parser Content
```Java
{
Name = "fireeye-networksecurity-json-network-traffic-success-smb2"
	Conditions = [ """"event_type":"smb2"""", """"flow_id":""", """"smb2":{""", """"command_str":"""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
    	"""exa_json_path=$.smb2.command_str,exa_field_name=command""",
    	"""exa_json_path=$.smb2.pid,exa_field_name=process_id""",
    	"""exa_json_path=$.smb2.sid,exa_field_name=session_id""",
    	"""exa_json_path=$.smb2.mid,exa_field_name=message_id""",
    	"""exa_regex="smb2":\{[^\}]+?"command_str":"(?i)({access}create|write|close|read)"[^}]+?"\w+":\{[^}]*?"fid":"({file_id}[^"]+)"""",
    	"""exa_regex="smb2":\{[^\}]+?"command_str":"(?i)({access}create|write|close|read)"[^}]+?"\w+":\{[^}]*?"filename":"({file_path}((|({file_dir}[^"]*?)[\\\/]+))?({file_name}[^"\\\/]+?(\.({file_ext}[^"\/\\\.]+))?))""""
    ]
	ParserVersion = "v1.0.0"

fireeye-networksecurity-nx-events = {
  Vendor = FireEye
  Product = FireEye Network Security (NX)
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.iface,exa_field_name=interface_name""",
    """exa_json_path=$.session_key,exa_field_name=session_id""",
    """exa_json_path=$.event_type,exa_field_name=event_category""",
    """exa_json_path=$.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)""",
    """exa_json_path=$.src_port,exa_field_name=src_port""",
    """exa_json_path=$.dest_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)""",
    """exa_json_path=$.dest_port,exa_field_name=dest_port""",
    """exa_json_path=$.proto,exa_field_name=protocol""",
    """exa_json_path=$.app_proto,exa_field_name=app_protocol"""
  
}
```