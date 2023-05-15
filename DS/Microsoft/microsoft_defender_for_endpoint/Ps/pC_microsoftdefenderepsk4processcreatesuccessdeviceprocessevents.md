#### Parser Content
```Java
{
Name = microsoft-defenderep-sk4-process-create-success-deviceprocessevents
  Conditions = [""""FileName":""", """requestClientApplication=""", """AdvancedHunting-DeviceProcessEvents"""]
  Fields = ${MicrosoftParserTemplates.cef-defender-atp-2.Fields} [
     """ProcessId":({process_id}\d+)""",
     """InitiatingProcessFileName":\s*"({parent_process}[^"]+)""",
     """"FileName":\s*"({process_name}[^"]+)""",
     """DeviceName":\s*"({dest_host}[^"]+)""",
     """ProcessCommandLine":\s*"({process_command_line}[^"]+)\s*""""
     """MD5":"({hash_md5}[^"]+)""",
 ]
 ParserVersion = "v1.0.0"

cef-defender-atp-2 = {
     Vendor = Microsoft
     Product = Microsoft Defender for Endpoint
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
     Fields = [
       """time"+:\s*"+({time}[^"]+)"""",
       """operationName"+:\s*"+({operation}[^"]+)""",
       """category"+:\s*"+({category}[^"]+)""",
       """RemotePort"+:({dest_port}\d+)""",
       """RemoteIP"+:\s*"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
       """"Protocol"+:\s*"+({protocol}[^"]+)""",
       """LocalIP"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """LocalPort"+:({src_port}\d+)""",
       """ActionType"+:\s*"+({result}[^"]+)""",
       """DeviceName"+:\s*"+({dest_host}[^"]+)""",
       """InitiatingProcessAccountName"+:\s*"+((?i)SYSTEM|(?i)network service|({user}[^"]+))""",
       """"ProcessIntegrityLevel"+:\s*"+({process_integrity}[^"]+)""",
       """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
       """"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]+))""""
       """InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)""",
     ]
     DupFields = ["category->event_name"
}
```