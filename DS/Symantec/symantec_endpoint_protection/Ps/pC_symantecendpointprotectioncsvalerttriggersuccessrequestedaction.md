#### Parser Content
```Java
{
Name = symantec-endpointprotection-csv-alert-trigger-success-requestedaction
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,实际的操作:""",""",请求的操作:""" ]
  Fields = [
         """计算机名:\s*(?:0+|({host}[^,]+))""",
         """事件时间:\s*({time}[\d\- :]+)""",
         """({alert_type}(发现病毒|发现安全风险))""",
         """IP 地址:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
         """风险名称:\s*({alert_name}[^,]+)""",
         """出现次数:\s*\d+,({malware_url}[^,]+)""",
         """用户:\s*({user}[^,]+)""",
         """计算机名:\s*(?:0+|({src_host}[^,]+))""",
         """源计算机:\s*(?:0+|({dest_host}[^,]+))?,""",
         """源 IP:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
         """可信度:\s*({additional_info}[^,]+)\s*"""
        ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_type->malwareCategory", "src_host->malwareVictimHost", "malware_url->malwareAttackerUrl", "dest_ip->malwareAttackerIp"]
    NameTemplate = """Symantec Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```