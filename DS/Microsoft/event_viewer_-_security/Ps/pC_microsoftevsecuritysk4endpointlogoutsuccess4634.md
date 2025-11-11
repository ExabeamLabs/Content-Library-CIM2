#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-endpoint-logout-success-4634
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  Conditions = [  """'NetApp-Security-Auditing'""", """'EventID': 4634""", """'Computer'"""  ]
  Fields = ${DLWindowsParsersTemplates.netapp-json-windows-events.Fields} [
    """'SubjectDomainName':\s+'({src_domain}[^']+)""",
    """'TargetDomainName':\s+'({dest_domain}[^']+)""",
    """'SubjectIP':\s+'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """'SubjectUserName':\s+'({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """'TargetUserName':\s+'({dest_user}[^']+)""",
    """'IpAddress':\s+'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """'Computer':\s+'({src_host}({host}[\w\-\.]+))"""
    """'TargetUserName':\s+'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """'TargetDomainName':\s+'({domain}[^']+)""",
  ]

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
    """'SubjectUserSid':\s+'({user_sid}[^']+)""",
    """'ObjectServer':\s+'({object_server}[^']+)""",
    """'ObjectType':\s+'({object_class}[^']+)""",
    """'HandleID':\s+'({handle_id}[^']+)""",
    """'ObjectName':\s+'({object}[^']+)""",
    """'AccessList':\s+'({access}.+?)\s+'""",
    """'AccessMask':\s+({access_mask}\d+)""",
    """'@SystemTime':\s+'({time}[^']+)"""
    """'IpPort':\s+({src_port}\d+)""",
    """'TargetUserSID':\s+'({dest_user_sid}[^']+)""",
    """'AuthenticationPackageName':\s+'({auth_package}[^']+)""",
    """'LogonType':\s+({login_type}\d+)""",
    """'Provider':.+?@Name':\s+'({provider_name}[^']+)""",
    """'Provider':.+?@Guid':\s+'({provider_guid}[^']+)""",
    """'ObjectName':\s+'({file_path}[^']+)""",
    """'ObjectName':\s+'[^.]+\/({file_name}[^']+?(\.({file_ext}[^\s\.']+))?)'""",
    """'OldSD':\s+'({old_sd}[^']+)""",
    """'NewSD':\s+'({new_sd}[^']+)"""
    
}
```