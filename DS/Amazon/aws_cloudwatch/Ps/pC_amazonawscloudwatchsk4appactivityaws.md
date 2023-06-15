#### Parser Content
```Java
{
Name = amazon-awscloudwatch-sk4-app-activity-aws
  Vendor = Amazon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ParserVersion = v1.0.0
  Product = AWS CloudWatch
  Conditions = [ """destinationServiceName =AWS""", """dproc=CloudWatch""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z)""",
    """destinationServiceName =({app}[^=]+?)\s+(\w+=|$)""",
    """dproc=({process_name}[^=]+?)\s+(\w+=|$)""",
    # log_level is removed
    """"TenantId":"({tenant_id}[^"]+)""",
    """"Computer":"({host}[^"]+)""",
    """"(H|h)ost(N|n)ame_s":"({host}[^"]+)""",
    # src_system is removed
    """"(?i)Type":"({event_category}[^"]+)""",
    """"Computer":"({computer_name}[^"]+)""",
    """"Account":"(({domain}[^"]+?)[\\\/]+)?({user}[^"\\\/]+)"""",
    # mg is removed
    """"ManagementGroupName":"({group_name}[^"]+)""",
    """"_ResourceId":"({resource_id}[^"]+)""",
    # code_cf is removed
    """"ClusterName_s":"({cluster_name}[^"]+)""",
    # cluster_type is removed
    # full_log is removed
    # full_log is removed
    """Activity":"({event_name}[^"]+?)\s*"""",
    """message":"({event_name}[^"]+?)\s*"""",
    """errorCode":"({error_code}[^"]+)""",
    # full_log is removed
    """"Message":"\[({additional_info}[^\]]+?)\s*\]""",
    # full_log is removed
    """"Message":"\[({event_name}[^\]]+)""",
    """"\$table":"({table}[^"]+)""",
    """User Agent - ({user_agent}.+?)\s+\[""",
    """"sourceIPs":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"userAgent":"({user_agent}[^"]+)"""",
    """"code":({response_code}\d+)""",
    """"AlertSeverity":"({alert_severity}[^",]+)""",
    """"AlertName":"({alert_name}[^",]+)""",
    """"RiskScore"+:\s*"+({alert_severity}[^",]+)""",
    """"Process":"({process_name}[^"]+)"""
  ]


}
```