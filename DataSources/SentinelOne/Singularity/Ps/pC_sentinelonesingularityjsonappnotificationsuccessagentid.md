#### Parser Content
```Java
{
Name = sentinelone-singularity-json-app-notification-success-agentid
  Vendor = SentinelOne
  Product = Singularity
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"modular_input_consumption_time":""", """"timestamp":""", """"agentId":""" ]
  Fields = [
    """"createdAt":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"updatedAt":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"(computerName|agentComputerName)":\s*"({src_host}[^"]+)"""",
    """"(osType|agentOsType)":\s*"({os}[^"]+)"""",
    """"agentMachineType":\s*"({host_type}[^"]+)"""",
    """"agentNetworkStatus":\s*"({result}[^"]+)"""",
    """"publisher":\s*"({domain}[^"]+)"""",
    """"name":\s*"({app}[^"]+?)\s*"""",
    """"type":\s*"({file_type}[^"]+)"""",
    """"accountName":\s*"({account}[^"]+)"""",
    """"primaryDescription":\s*"({additional_info}[^"]+)"""",
    """"agentDomain":\s*"({src_domain}[^"]+)""""
  ]


}
```