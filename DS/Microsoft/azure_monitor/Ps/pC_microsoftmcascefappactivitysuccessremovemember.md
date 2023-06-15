#### Parser Content
```Java
{
Name = microsoft-mcas-cef-app-activity-success-removemember
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Remove member from group|"""
]
ParserVersion = "v1.0.0"

ms-azure-eventhubs-activity.Fields}[
    """({category}Device)""",
    """"operationType":"({operation_type}[^",]+)""""
  ]
  ParserVersion = "v1.0.0"
},

${MSParsersTemplates.ms-azure-eventhubs-activity} {
  Name = microsoft-azure-json-app-activity-updateuser
  Conditions= [ """"category":"UserManagement"""", """"operationName":"Update user"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}UserManagement)"""
  ]
  ParserVersion = "v1.0.0"
},

${MSParsersTemplates.ms-azure-eventhubs-activity} {
  Name = microsoft-azure-json-app-activity-updategroup
  Conditions= [ """"category":"GroupManagement"""", """"operationName":"Update group"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}GroupManagement)"""
  ]
  ParserVersion = "v1.0.0"
},

${MSParsersTemplates.ms-azure-eventhubs-activity} {
  Name = microsoft-azure-json-app-activity-addgroup
  Conditions= [ """"category":"GroupManagement"""", """"operationName":"Add group"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}GroupManagement)"""
  ]
  ParserVersion = "v1.0.0"
},

${MSParsersTemplates.ms-azure-eventhubs-activity} {
  Name = microsoft-azure-json-app-activity-groupmanagement
  Conditions= [ """"category":"GroupManagement"""", """"operationName":"Add owner to group"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}GroupManagement)"""
  ]
  ParserVersion = "v1.0.0"
},

${MSParsersTemplates.ms-azure-eventhubs-activity} {
  Name = microsoft-azure-json-app-activity-deletegroup
  Conditions= [ """"category":"GroupManagement"""", """"operationName":"Delete group"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}GroupManagement)"""
  ]
  ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Azure Monitor
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"ResourceProvider":"({object}[^"]+)"""
  """"ResourceId":"({file_path}({file_dir}(?:[^";]+)?[\/;])?({file_name}[^\/";]+))""""
  """"Resource":"({file_name}[^"]+)""""
  """"id_s":"({file_path}({file_dir}(?:[^";]+)?[\/;])?({file_name}[^\/";]+)?)""""
  """"SourceSystem":"({app}[^"]+)""""
  """"CallerIPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"ResultType":"({result}[^"]+)"""
  """"OperationName":"({event_name}[^"]+)""""
  """"identity_claim_unique_name_s":"(({email_address}[^@"]+@[^\.]+\.[^"]+)|({user}[^"]+))""""
  """suser=({email_address}[^=@]+@[^\.]+\.[^\s=]+)"""
  """"ResourceId":"({file_path}({file_dir}(?:[^";]+)?[\/;])?({file_name}[^\/";]+))""""
]
Name = microsoft-azure-sk4-file-read-success-vaultget
Conditions = [
  """destinationServiceName =Azure"""
  """"_ResourceId":""""
  """"CorrelationId":""""
  """dproc=Log Analytics OMS Workspace"""
  """"OperationName":"VaultGet""""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=.*?\s+folder\s+(\([^\)]*\):\s*)?({object}.*?)\s+(\w+=|$)"""
  """\WrequestClientApplication=(|({user_agent}.*?))\s+(\w+=|$)"""
]
Name = microsoft-mcas-cef-app-activity-success-purgemessages
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Purge messages from the mailbox|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=.*?\s+folder\s+(\([^\)]*\):\s*)?({object}.*?)\s+(\w+=|$)"""
  """\WrequestClientApplication=(|({user_agent}.*?))\s+(\w+=|$)"""
]
Name = microsoft-mcas-cef-app-activity-success-removemember
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Remove member from group|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=.*?\s+folder\s+(\([^\)]*\):\s*)?({object}.*?)\s+(\w+=|$)"""
  """\WrequestClientApplication=(|({user_agent}.*?))\s+(\w+=|$)"""
]
Name = microsoft-mcas-cef-app-activity-success-unspecified
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Unspecified|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=.*?\s+folder\s+(\([^\)]*\):\s*)?({object}.*?)\s+(\w+=|$)"""
  """\WrequestClientApplication=(|({user_agent}.*?))\s+(\w+=|$)"""
]
Name = microsoft-mcas-cef-app-activity-success-mailboxpermission
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Add recipient mailbox permission|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=.*?\s+folder\s+(\([^\)]*\):\s*)?({object}.*?)\s+(\w+=|$)"""
  """\WrequestClientApplication=(|({user_agent}.*?))\s+(\w+=|$)"""
]
Name = microsoft-mcas-cef-app-activity-success-azureoperation
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Azure operation|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@[^@\s]+)\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?)))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)"""
]
Name = microsoft-mcas-cef-file-delete-success-deletefile
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Delete file|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@[^@\s]+)\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({src_file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?)))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)"""
]
 DupFields = ["src_file_name->file_name" ]
Name = microsoft-mcas-cef-file-download-success-downloadfile
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Download file|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@[^@\s]+)\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({src_file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?)))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)"""
]
DupFields = ["src_file_name->file_name" ]
Name = microsoft-mcas-cef-file-download-success-syncfiledownload
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Sync file download|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Microsoft CAS
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@[^@\s]+)\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({src_file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?)))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)"""
]
DupFields = ["src_file_name->file_name" ]
Name = microsoft-mcas-cef-file-upload-success-uploadfile
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Upload file|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Microsoft"
Product = "Microsoft CAS"
TimeFormat = "epoch"
Fields = [
  """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
  """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s]+@[^@\s]+)\s+(\w+=|$)"""
  """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
  """\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?)))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)"""
]
Name = "microsoft-mcas-cef-file-read-success-mcas"
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Access file|"""
]
ParserVersion = "v1.0.0"
},


${MSParsersTemplates.cef-azure-onedrive-app-activity}{
  Name = microsoft-mcas-cef-app-activity-success-folderdelete
  TimeFormat = "epoch"
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|MCAS|SIEM_Agent|""", """|Delete folder|""" ]
  Fields = ${MSParsersTemplates.cef-azure-onedrive-app-activity.Fields} [
    """\Wrt=({time}\d{13})""",
  
}
```