#### Parser Content
```Java
{
Name = microsoft-defenderep-json-process-create-success-processevents
  Conditions = [  """"Type":"AdvancedHuntingDeviceProcessEvents_CL""", """TimeGenerated""", """TenantId""" ]
ParserVersion = "v1.0.0"

defender-atp-events {
   Vendor = Microsoft
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Fields = [
     """TimeGenerated"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
     """TenantId"*:\s*"*({host}[^"]+)""",
     """Computer"*:"*({host}[^"]+)""",
     """InitiatingProcessId_d"+:"+({process_id}\d+)""",
     """"Type"+:\s*"+({category}[^",]+)""",
     """RemotePort_d"+:({dest_port}\d+)""",
     """RemoteIP_s"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """"Protocol_s"+:\s*"+({protocol}[^"]+)""",
     """LocalIP_s"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """LocalPort_d"+:({src_port}\d+)""",
     """ActionType_s"+:\s*"+({result}[^",]+)""",
     """RemoteIPType_s"+:\s*"+(null|({direction}[^",]+))""",
     """DeviceName_s"+:\s*"+({dest_host}[\w\-.]+)""",
     """InitiatingProcessAccountName_s"+:\s*"+(system|SYSTEM|({user}[\w\.\-]{1,40}\$?))""",
     """"ProcessIntegrityLevel_s"+:\s*"+({process_integrity}[^",]+)""",
     """InitiatingProcessAccountSid_s"+:\s*"+({user_sid}[^",]+)""",
     """InitiatingProcessFileName_s"+:\s*"+({parent_process}[^",]+)""",
     """InitiatingProcessParentFileName_s"*:\s*"*({process_name}[^",]+)""",
     """InitiatingProcessCommandLine_s"*:"*({process_command_line}.+?)\s"","*(\w+"|$)""",
     """InitiatingProcessMD5_g"*:"*({hash_md5}[^",]+)""",
     ]
     DupFields = ["category->event_name"
}
```