#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-endpoint-activity-success-4660
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  Conditions = [  """'NetApp-Security-Auditing'""", """'EventID': 4660""", """'Computer'"""  ]
  Fields = ${DLWindowsParsersTemplates.netapp-json-windows-events.Fields} [
    """'Computer':\s+'({host}[\w\-\.]+)"""
  ]
  DupFields = [ "host->src_host", "src_user->user", "src_domain->domain" ]

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
    """'SubjectIP':\s+'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """'SubjectUserSid':\s+'({user_sid}[^']+)""",
    """'SubjectDomainName':\s+'({src_domain}[^']+)""",
    """'SubjectUserName':\s+'({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
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
    """'ObjectName':\s+'[^.]+\/({file_name}[^']+?(\.({file_ext}[^\s\.']+))?)'""",
    """'OldSD':\s+'({old_sd}[^']+)""",
    """'NewSD':\s+'({new_sd}[^']+)"""
        """'IpAddress':\s+'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    
}
```