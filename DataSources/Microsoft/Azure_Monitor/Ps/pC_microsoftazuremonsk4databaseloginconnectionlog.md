#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-database-login-connectionlog
  Product = Azure Monitor
  Conditions = [ """destinationServiceName =Azure""", """"category":"MySqlAuditLogs"""", """"event_class":"connection_log"""" ]
  Fields = ${MicrosoftParserTemplates.cef-azure-db-for-mysql.Fields}[
    """"db":"({db_name}[^",]+)""",
    """"connection_id":({connection_id}\d+)"""
  ]
  ParserVersion = "v1.0.0"

cef-azure-db-for-mysql = {
   Vendor = Microsoft
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
   Fields = [
     """"LogicalServerName":"({host}[^",]+)""",
     """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
     """"user":"({user}[\w\-]+)""",
     """"resourceId":"({resource}[^",]+)""",
     """"event_subclass":"({action}[^",]+)""",
     """"ip":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
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
  Product = SQL Server
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """\WComputerName =({host}[^=\s]+)""",
    """\WEventCode=({event_code}\d+)""",
    """\WSourceName =({service_name}.+?)(\s+\w+=|\s*$)""",
    """\Wsucceeded:({result}[^:\s]+)""",
    """\Wevent_time:({time}\d+\-\d+\-\d+ \d+:\d+:\d+\.\d{3})""",
    """\WUser=({user}[^\s]+?)(\s+\w+=|\s*$)""",
    """\WSid=({user_sid}[^\s]+?)(\s+\w+=|\s*$)""",
    """\Wserver_principal_name:(({domain}[^\\\/]+?)[\\\/])?({db_user}[^\\\/\s]+?)(\s+\w+:|\s*$)""",
    """\Wserver_principal_sid:({db_user_sid}[^\s]+)""",
    """\Wserver_instance_name:({dest_host}[^\s]+)""",
    """\Wadditional_information:.*?<address>({src_ip}[a-fA-F\d.:]+)""",
    """\Wdatabase_name:({db_name}[^\s]+)""",
    """\Wstatement:({failure_reason}[^.]+)"""
  ]
 },

  cef-defender-atp-2 = {
     Vendor = Microsoft
     Product = Defender ATP
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
     Fields = [
       """time"+:\s*"+({time}[^"]+)"""",
       """operationName"+:\s*"+({operation}[^"]+)""",
       """category"+:\s*"+({category}[^"]+)""",
       """RemotePort"+:({dest_port}\d+)""",
       """RemoteIP"+:\s*"+({dest_ip}[^"]+)""",
       """"Protocol"+:\s*"+({protocol}[^"]+)""",
       """LocalIP"+:\s*"+({src_ip}[^"]+)""",
       """LocalPort"+:({src_port}\d+)""",
       """ActionType"+:\s*"+({action}[^"]+)""",
       """RemoteIPType"+:\s*"+(null|({direction}[^"]+))""",
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