#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-file-success-accessanobject"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
ExtractionType = json
Conditions = [
"""An attempt was made to access an object."""
"""computer_name"""
]
Fields = [
"""({event_name}An attempt was made to access an object)"""
""""(?:winlog\.)?computer_name\\*":\\*"({dest_host}({host}[\w\-.]+))"""
"""@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({event_code}4663)"""
"""Object(:|=).*?Object Type(:|=)\s*({file_type}.+?)[\s;]*Object Name(:|=)\s*({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;\\]+?))?))[\s;]*Handle ID(:|=)"""
"""Process Name(:|=)\s*(?:|({process_path}.+?))[\s;]*Access Request Information(:|=)"""
"""Process Name(:|=).*\\({process_name}[^\\;]+?)[\s;]*Access Request Information(:|=)"""
"""Accesses(:|=)\s*({access}.+?)[\s;]*Access Mask(:|=)\s*({access_mask}\w+)"""
""""AccessList\\*":\\*"({access}[^"]+?)\s*""""
""""Account\\*":\\*"(({domain}[^\\\s"]+)\\+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""""SubjectUserSid\\*":\\*"({user_sid}[^\s"]+)"""
""""SubjectLogonId\\*":\\*"({login_id}[^\s"]+)"""
""""ObjectName\\*":\\*"(-|({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;]+?))?)))\s*""""
""""ObjectType":"(-|({file_type}[^\s"]+))"""
""""ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*""""
""""record_number"\s*:\s*\"({event_id}\d+)"""
""""SubjectUserName"\s*:\s*\"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""""SubjectDomainName"\s*:\s*\"({src_domain}({domain}[^\"]+))"""
""""ObjectName"\s*:\s*\"(?:({file_dir}[^\"]+?)\\+[^\"\\]+)""""
""""AccessList"\s*:\s*\"({access}.+?)""""
"""Access Request Information:[rnt\\]*Accesses:\s*((\\)*(\\t|\\r|\\n))*({access}[^\\]+)((\\)*(\\t|\\r|\\n))*Access Mask:\s*((\\)*(\\t|\\r|\\n))*({access_mask}[^"\s]+)\s*((\\)*(\\t|\\r|\\n))*"""
"""exa_json_path=$.message_info,exa_field_name=event_name"""
"""exa_json_path=$.@timestamp,exa_field_name=time"""
"""exa_json_path=$.event_id,exa_field_name=event_code"""
"""exa_json_path=$.event_data.ObjectType,exa_field_name=file_type"""
"""exa_regex=@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""exa_json_path=$.event_data.ObjectName,exa_regex=(-|({file_path}({file_dir}[^"]+\\)?({file_name}[^"]+(\.({file_ext}[^"]+)?))))"""
"""exa_json_path=$.event_data.ProcessName,exa_regex=(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+)))\s*"""
"""exa_json_path=$.record_number,exa_field_name=event_id"""
"""exa_json_path=$.event_data.SubjectUserName,exa_field_name=user"""
"""exa_json_path=$.event_data.SubjectUserName,exa_field_name=src_user"""
"""exa_json_path=$.event_data.SubjectDomainName,exa_field_name=domain"""
"""exa_json_path=$.event_data.SubjectDomainName,exa_field_name=src_domain"""
"""exa_json_path=$.event_data.ObjectName,exa_regex=(?:({file_dir}[^"]+)\\+[^\"\\]+)"""
"""exa_json_path=$.event_data.AccessList,exa_regex=({access}[^\\]+?)(\n|\r\t)"""
"""exa_json_path=$.event_data.SubjectUserSid,exa_field_name=user_sid"""
"""exa_json_path=$.computer_name,exa_field_name=host"""
"""exa_json_path=$.computer_name,exa_field_name=dest_host"""
"""exa_json_path=$.event_data.AccessMask,exa_field_name=access_mask"""
"""exa_json_path=$.event_data.SubjectLogonId,exa_field_name=login_id"""
]
ParserVersion = "v1.0.0"


}
```