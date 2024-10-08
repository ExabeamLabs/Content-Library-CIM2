#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-permission-modify-4670-1
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  ExtractionType = json
  Conditions = [  """EventID":"4670"""", """Permissions on an object were changed""" ]
  Fields =${DLWindowsParsersTemplates.json-windows-system-events.Fields}[
    """exa_json_path=$.Computer,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$..HandleId,exa_field_name=object_id""",
    """exa_json_path=$..ObjectType,exa_field_name=object_type""",
    """exa_json_path=$..ObjectName,exa_regex=^(?:-|({object_name}[^"]+))$""",
    """exa_json_path=$..NewSd,exa_field_name=attribute""",
    """exa_json_path=$..Category,exa_field_name=category""",
    """exa_json_path=$..Opcode,exa_field_name=severity"""
  ]
  DupFields = ["process_name -> file_name"]

json-windows-system-events = {
  Vendor = Microsoft
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """exa_json_path=$.EventID,exa_field_name=event_code""",
    """exa_json_path=$.EventTime,exa_regex=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """exa_json_path=$.TimeCreated,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.TimeCreated,exa_field_name=time""",
    """exa_json_path=$.Hostname,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.EventType,exa_field_name=result""",
    """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
    """exa_json_path=$..SubjectUserName,exa_regex=^({user}[\w\.\-]{1,40}\$?)$""",
    """exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
    """exa_json_path=$..SubjectLogonId,exa_field_name=login_id""",
    """exa_json_path=$..ProcessId,exa_field_name=process_id""",
    """exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$""",
    """exa_json_path=$..param1,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$""",
    """exa_json_path=$..TransactionId,exa_field_name=transaction_id""",
    """exa_json_path=$..Category,exa_field_name=event_name""",
    """exa_json_path=$..Message,exa_regex=({event_name}[^.]+)"""
  
}
```