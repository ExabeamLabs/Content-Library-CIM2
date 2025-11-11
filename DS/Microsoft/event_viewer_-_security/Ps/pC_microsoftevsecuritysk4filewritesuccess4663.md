#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-file-write-success-4663
  Product = Event Viewer - Security
  Conditions = [ """EventID': 4663""", """'NetApp-Security-Auditing'""", """'Computer'""" ]
  Fields = ${WindowsParsersTemplates.netapp-json-windows-events-1.Fields}[
    """'SubjectIP':\s+'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """'SubjectUserName':\s+'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """'SubjectDomainName':\s+'({domain}[^']+)""",
    """'TargetDomainName':\s+'({dest_domain}[^']+)""",
    """'TargetUserName':\s+'({dest_user}[^']+)""",
    """'IpAddress':\s+'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?',""",
    """'Computer':\s+'({host}[\w\-\.]+)"""
  ]
  ParserVersion = "v1.0.0"

netapp-json-windows-events-1 = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSS"
  Fields = [
    """'EventID':\s+({event_code}\d+)"""
    """'EventName':\s+'({event_name}({access}[^']+))"""
    """'Opcode':\s+({opcode}\d+)""",
    """'Keywords':\s+'({keywords}[^']+)""",
    """'Result':\s+'({result}[^']+)""",
    """'ComputerUUID':\s+'({user_uid}[^']+)""",
    """'SubjectUserSid':\s+'({user_sid}[^']+)""",
    """'ObjectServer':\s+'({object_server}[^']+)""",
    """'ObjectType':\s+'({file_type}({object_class}[^']+))""",
    """'HandleID':\s+'({handle_id}[^']+)""",
    """'ObjectName':\s+'({object}[^']+)""",
    """'AccessList':\s+'({event_name}({access}.+?))\s*'""",
    """'AccessMask':\s+({access_mask}\d+)""",
    """'@SystemTime':\s+'({time}[^']+)"""
    """'IpPort':\s+({src_port}\d+)""",
    """'TargetUserSID':\s+'({dest_user_sid}[^']+)""",
    """'AuthenticationPackageName':\s+'({auth_package}[^']+)""",
    """'LogonType':\s+({login_type}\d+)""",
    """'Provider':.+?@Name':\s+'({provider_name}[^']+)""",
    """'Provider':.+?@Guid':\s+'({provider_guid}[^']+)""",
    """'ObjectName':\s+'(({registry_path}\\+REGISTRY[^']+?({registry_key}[^'\\\/]+))|({file_path}[^']+?({file_name}[^\\\/]+(\.({file_ext}[^\s'\.]+)))?))'""",
    """'OldSD':\s+'({old_sd}[^']+)""",
    """'NewSD':\s+'({new_sd}[^']+)"""    
}
```