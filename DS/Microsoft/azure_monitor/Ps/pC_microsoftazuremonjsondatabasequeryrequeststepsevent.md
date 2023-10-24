#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-query-requeststepsevent
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"RequestSteps"""",
    """"operationName":"RequestStepsEvent""""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
    """"Command":"({db_query}.+?)\s*"""",
	  """"StartTime":"({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  ]

cef-azure-db-for-mysql = {
   Vendor = Microsoft
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
   Fields = [
     """"LogicalServerName":"({host}[^",]+)""",
     """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
     """"user":"({user}[\w\.\-]{1,40}\$?)""",
     """"resourceId":"({resource}[^",]+)""",
     """"event_subclass":"({action}[^",]+)""",
     """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"ResourceGroup":"({server_group}[^"]+)""",
     """"SubscriptionId":"({subscription_id}[^"]+)""",
# resource_provider is removed
     """"category":"({category}[^"]+)""",
     """"operationName":"({action}[^"]+)""",
     """\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
   ]
   DupFields = ["action->operation","event_hub_namespace->host"]
 },

s-mssql-database-login = {
  Vendor = Microsoft
  Product = MSSQL
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """\WComputerName =({host}[^=\s]+)""",
    """<Computer>({host}[\w\-.]+)<"""
    """\WEventCode=({event_code}\d+)""",
    """\WSourceName =({service_name}.+?)(\s+\w+=|\s*$)""",
    """succeeded\\?:({result}[^:\s\\]+)""",
    """event_time:({time}\d+\-\d+\-\d+ \d+:\d+:\d+\.\d{3})""",
    """\WUser=({user}[\w\.\-]{1,40}\$?)(\s+\w+=|\s*$)""",
    """\WSid=({user_sid}[^\s]+?)(\s+\w+=|\s*$)""",
    """\Wserver_principal_name:(({domain}[^\\\/]+?)[\\\/])?({db_user}[^\\\/\s]+?)(\s+\w+:|\s*$)""",
    """server_principal_sid:({db_user_sid}[^\s\\]+)""",
    """server_instance_name:({dest_host}[^\\\s]+)""",
    """additional_information:.*?<address>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdatabase_name:({db_name}[^\s]+)""",
    """\Wstatement:({failure_reason}[^.]+)"""
  ]
 },

  cef-defender-atp-2 = {
     Vendor = Microsoft
     Product = Microsoft Defender for Endpoint
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
     Fields = [
       """time"+:\s*"+({time}[^"]+)"""",
       """operationName"+:\s*"+({operation}[^"]+)""",
       """category"+:\s*"+({category}[^"]+)""",
       """RemotePort"+:({dest_port}\d+)""",
       """RemoteIP"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
       """"Protocol"+:\s*"+({protocol}[^"]+)""",
       """LocalIP"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """LocalPort"+:({src_port}\d+)""",
       """ActionType"+:\s*"+({result}[^"]+)""",
       """DeviceName"+:\s*"+({dest_host}[\w\-.]+)""",
       """InitiatingProcessAccountName"+:\s*"+((?i)SYSTEM|(?i)network service|({user}[\w\.\-]{1,40}\$?))""",
       """"ProcessIntegrityLevel"+:\s*"+({process_integrity}[^"]+)""",
       """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
       """"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]+))""""
       """InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)""",
     ]
     DupFields = ["category->event_name"
}
```