#### Parser Content
```Java
{
Name = microsoft-azuremon-cef-app-activity-category
  Conditions= [ """CEF:""", """destinationServiceName =Azure""", """"operationName":""", """"category":""" ]
  Fields = ${LMSMSParsersTemplates.cef-microsoft-app-activity.Fields}[
    """"path":"(-|({file_path}({file_dir}\/(\S+\/)?)({file_name}[^"\\\/]+)))\s*",""",
    """process":"({process_name}[^"]+)""",
    """ResourceId":"({resource}[^"]+)""",
# azure_event_hub_namespace is removed
# azure_event_hub_name is removed
    """(d|D)eviceName"+:\s*"+({dest_host}[\w\-.]+)""",
    """"resultType":"({result}[^"]+)"""",
    """Vendor":"({vendor_name}[^"]+?)"""",
    """"MD5"+:"+({hash_md5}[^"]+)"""",
    """"InitiatingProcessMD5"+:"+({hash_md5}[^"]+)"""",
    """"SHA1"+:"+({hash_sha1}[^"]+)"""",
    """"InitiatingProcessSHA1"+:"+({hash_sha1}[^"]+)"""",
    """"SHA256"+:"+({hash_sha256}[^",]+)"""",
    """"InitiatingProcessSHA256"+:"+({hash_sha256}[^",]+)"""",
    """"ProcessCommandLine"+:"+({process_command_line}.+?)\s*"+,""",
    """"InitiatingProcessCommandLine"+:"+({process_command_line}.+?)\s*"+,""",
    """"FileName"+:"+({file_name}[^"]+?(\.({file_ext}[^".]+))?)"""",
    """"FolderPath"+:"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
    """"InitiatingProcessVersionInfoOriginalFileName"+:"+({process_name}[^"]+)"""",
    """"InitiatingProcessParentFileName"+:"+({parent_process_name}[^"]+)"""",
    """"InitiatingProcessFileName"+:"+({process_name}[^"]+)"""",
    """"InitiatingProcessFolderPath"+:"+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))"""",
    """"InitiatingProcessVersionInfoProductName"+:"+({product_name}[^"]+)"""",
    """"RegistryKey"+:"+({registry_path}({registry_key}[^"]+))"""",
    """"RegistryValueName"+:"+({registry_value}[^"]+)""""
    """"FileName":"(null|({file_name}[^"]+(\.({file_ext}[^".]+))))?""""
    """"AccountName":"(null|({account}[^"]+))""""
    """"MachineGroup":"({group_name}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"

cef-microsoft-app-activity = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"Host":"({host}[^"]+)"""",
    """"message":"({additional_info}[^"]+)""",
    """"description":"({additional_info}[^"]+)""",
    """category":"({category}[^"]+)"""",
    """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """resourceId":\s*"({object}[^"]+)""",
    """"Operation":\s*"({operation}[^"]+)""",
    """"operationName":"({operation}[^"]+)""",
    """"name":"({full_name}[^"]+)"""",
    """action":"({action}[^"]+)""",
    """"((?i)callerIpAddress|CIp)":"({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))(:({src_port}\d+))?"""",
    """claims\/(name|upn)":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"email":"({email_address}[^\s@"]+@[^\s@"]+)""",
    """({app}Databricks)""",
    """"serviceName\\*":\\*"({app}[^"]+)""",
    """destinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
# port is removed
    """"(?i)userAgent":"({user_agent}[^"]+)"""",
    """"statusCode\\":({http_response_code}\d+)""",
    """"actionName":"({operation}[^"]+)""",
    """(?i)userId":"({user_upn}[^",]+)""",
    """\[Namespace:\s*({host}\S+) ; EventHub name:"""
    """"UserType":"*({user_type}[^,}"]+)"*"""
    """"Platform":"({os}[^"]+)""""
    """"OriginatingServer":"({host}\w+)\s*(\([^\)]+?\))?(\\r\\n)?""""
    """"ClientInfoString":"({user_agent}[^"]+)","""
    """"BrowserName":"({browser}[^"]+)"""
    """"(Client|Source)IPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?""""
    """"Workload":\s*"({app}[^"]+)""""
    #"""duser=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"CorrelationId":\s*"({correlation_id}[^"]+)""""
  ]
  DupFields = [ "object->resource" 
}
```