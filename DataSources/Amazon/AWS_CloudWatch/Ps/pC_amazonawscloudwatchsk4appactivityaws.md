#### Parser Content
```Java
{
Name = amazon-awscloudwatch-sk4-app-activity-aws
  Vendor = Amazon
  ParserVersion = v1.0.0
  Product = AWS CloudWatch
  Conditions = [ """destinationServiceName =AWS""", """dproc=CloudWatch""" ]

cef-cloud-system-info = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z)""",
    """destinationServiceName =({app}[^=]+?)\s+(\w+=|$)""",
    """dproc=({process_name}[^=]+?)\s+(\w+=|$)""",
# log_level is removed
    """"TenantId":"({tenant_id}[^"]+)""",
    """"Hostname_s":"({host}[^"]+)""",
# src_system is removed
    """"Type":"({event_category}[^"]+)""",
    """"Computer":"({computer_name}[^"]+)""",
# mg is removed
    """"ManagementGroupName":"({group_name}[^"]+)""",
    """"_ResourceId":"({resource_id}[^"]+)""",
# code_cf is removed
    """"ClusterName_s":"({cluster_name}[^"]+)""",
# cluster_type is removed
# full_log is removed
    """Activity":"({event_name}[^"]+)""",
    """message":"({event_name}[^"]+)""",
    """errorCode":"({error_code}[^"]+)""",
# full_log is removed
    """"Message":"\[({event_name}[^\]]+)""",
    """"\$table":"({table}[^"]+)""",
    """User Agent - ({user_agent}.+?)\s+\[""",
    """"sourceIPs":\["({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """"userAgent":"({user_agent}[^"]+)"""",
    """"code":({result_code}\d+)""",
    """"AlertSeverity":"({alert_severity}[^",]+)""",
    """"AlertName":"({alert_name}[^",]+)""",
    """"RiskScore"+:\s*"+({alert_severity}[^",]+)"""
  ]
 
}
```