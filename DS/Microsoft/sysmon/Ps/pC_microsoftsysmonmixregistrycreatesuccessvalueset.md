#### Parser Content
```Java
{
Name = "microsoft-sysmon-mix-registry-create-success-valueset"
  Vendor = "Microsoft"
  Product = "Sysmon"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """Registry value set: """
	""" UtcTime: """
  ]
  Fields = [
    """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """\sComputer="({host}[\w\-.]+)""""
    """({host}[\w\-\.]+)\sMicrosoft-Windows-Sysmon"""
    """User=({user}.+?)\s+(\w+=|$)"""
    """Domain=({domain}.+?)\s+(\w+=|$)"""
    """User:\s*(?:(NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\]+))\\)?(SYSTEM|(NETWORK|LOCAL) SERVICE|({user}[^:]+?))\s+LogonGuid:"""
    """Sid=\s*({user_sid}[^\s]+)"""
    """LogonId:\s*({login_id}[^\s]+)"""
    """Hashes:\s*,?MD5=({hash_md5}[^\s,]+)"""
    """({event_name}Process Create)"""
    """\sProcessGuid:\s*\{({process_guid}[^\s\}]+)"""
    """\sProcessId:\s*({process_id}\d+)"""
    """ParentProcessGuid:\s*\{({parent_process_guid}[^\s\}]+)"""
    """CommandLine:\s*"*({process_command_line}.+?)\s*"*\s*CurrentDirectory:"""
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^:]+?))\s+(\w+:|$)"""
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^:]+?))\s+CommandLine:"""
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^:]+?))\s+FileVersion:"""
    """\s+ParentImage:\s*({parent_process}({parent_process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({parent_process_name}[^:]+?))\s+ParentCommandLine:"""
    """Event ID:\s*({event_code}\d+)"""
    """\s+Image:\s*({file_path}({file_dir}(?:(\w+:)?[^:]+)?[\\\/])?({file_name}.+?))\s+\w+:"""
    """TargetObject:\s*({object}({registry_path}({registry_key}.*)\\({registry_value}[^\\.]+(\.[^\\.]+?)?)))\s+Details:"""
    """Details:\s*({registry_details}.+?)\s*$"""
    """Details:\s*({registry_details_type}DWORD|QWORD|Binary Data)?\s*({registry_details}.+?)\s*$"""
    """ComputerName(:|=)\s*({host}[\w.-]+)"""
    """"({log_name}Microsoft-Windows-Sysmon)"""
  ]
  DupFields = [ 
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```