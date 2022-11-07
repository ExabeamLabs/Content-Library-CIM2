#### Parser Content
```Java
{
Name = netapp-n-sk4-file-permission-modify-4670
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =""", """'NetApp-Security-Auditing'""", """EventID': 4670"""  ]

netapp-json-windows-events = {
  Vendor = NetApp
  Product = NetApp
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSS"
  Fields = [
    """'EventID':\s+({event_code}\d+)"""
    """'EventName':\s+'({event_name}[^']+)"""
    """'Opcode':\s+({opcode}\d+)""",
    """'Keywords':\s+'({keywords}[^']+)""",
    """'Result':\s+'({result}[^']+)""",
    """'Computer':\s+'({host}[^']+)""",
    """'ComputerUUID':\s+'({user_uid}[^']+)""",
    """'SubjectIP':\s+'({src_ip}[^']+)""",
    """'SubjectUserSid':\s+'({user_sid}[^']+)""",
    """'SubjectDomainName':\s+'({domain}[^']+)""",
    """'SubjectUserName':\s+'({user}[^']+)""",
    """'ObjectServer':\s+'({object_server}[^']+)""",
    """'ObjectType':\s+'({object_class}[^']+)""",
    """'HandleID':\s+'({handle_id}[^']+)""",
    """'ObjectName':\s+'({object}[^']+)""",
    """'AccessList':\s+'({access}.+?)\s+'""",
    """'AccessMask':\s+({access_mask}\d+)""",
    """'@SystemTime':\s+'({time}[^']+)"""
    """'IpPort':\s+({src_port}\d+)""",
    """'TargetUserSID':\s+'({dest_user_sid}[^']+)""",
    """'TargetUserName':\s+'({dest_user}[^']+)""",
    """'TargetDomainName':\s+'({dest_domain}[^']+)""",
    """'AuthenticationPackageName':\s+'({auth_package}[^']+)""",
    """'LogonType':\s+({login_type}\d+)""",
    """'Provider':.+?@Name':\s+'({provider_name}[^']+)""",
    """'Provider':.+?@Guid':\s+'({provider_guid}[^']+)""",
    """'ObjectName':\s+'({file_path}[^']+)""",
    """'ObjectName':\s+'[^.]+\/({file_name}[^']+)""",
    """'OldSD':\s+'({old_sd}[^']+)""",
    """'NewSD':\s+'({new_sd}[^']+)"""
    
}
```