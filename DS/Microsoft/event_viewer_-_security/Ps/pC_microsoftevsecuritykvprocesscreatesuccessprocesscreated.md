#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-processcreated
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"__li_source_path="""", """"A new process has been created"""","""eventid="4688"""" ]
  Fields = [
    """({event_name}A new process has been created)""",
    """__li_source_path="({host}[^"]+)"""",
    """__li_source_path="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """({event_code}4688)""",
    """Process Name:\s+({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))\s+Token Elevation Type:""",
    """Process Name:\s+({path}.+?)\s+Token Elevation Type:""",
    """Account Name:\s+({user}.+?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)""",
    """New Process ID:\s+({process_guid}[^\s]+)\s""",
    """Creator Process ID:\s+({parent_process_guid}[^\s]+)\s""",
    """Process Command Line:\s+"({process_command_line}[^"]+)"\s""",
    """Process Command Line:\s+"(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= ({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))"\s""",
    """TaskCategory=({operation_type}Process Creation)"""
    ]
  DupFields = [ "process_guid->process_id" ]


}
```