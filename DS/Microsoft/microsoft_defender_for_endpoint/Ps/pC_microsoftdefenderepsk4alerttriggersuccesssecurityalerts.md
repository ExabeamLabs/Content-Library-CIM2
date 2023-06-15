#### Parser Content
```Java
{
Name = microsoft-defenderep-sk4-alert-trigger-success-securityalerts
   ParserVersion = v1.0.0
   Vendor = Microsoft
   Product = Microsoft Defender for Endpoint
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Conditions = [ """dproc=Graph Security Alerts""", """provider":"Microsoft Defender ATP""" ]
   Fields = [
     """\s({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)\s+[^\s]+\s+""",
     """"+hostStates"+:[^\}\]]+?fqdn"+:"+({host}[^"]+)""",
     """"+hostStates"+:[^\}\]]+?privateIpAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"+hostStates"+:[^\}\]]+?publicIpAddress"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
     """"+hostStates"+:[^\}\]]+?riskScore"+:"+({alert_severity}[^"]+)""",
     """"+hostStates"+:[^=]+?accountName"+:"+({user}[^"]+)""",
     """"+hostStates"+:[^=]+?domainName"+:"+({domain}[^"]+)""",
     """"+hostStates"+:[^=]+?userPrincipalName"+:"+({email_address}[^@"]+@[^"]+)"""",
     """recommendedActions"+[^=]+?severity"+:"+({alert_severity}[^"]+)""",
     """recommendedActions"+[^=]+?title"+:"+({alert_name}[^"]+)""",
     """"+category"+:"+({alert_type}[^"]+)""",
     """"+fileHash"+[^\}\]]+?hashValue"+:"+({sha1_sum}[^"]+)""",
     """"+description"+:"({additional_info}[^"]+?)\s*"""",
     """"+sourceMaterials"+:\["+({additional_info}[^"]+)""",
     """"id"+:"+({alert_id}[^"]+)""""
   ]
   DupFields = [ "host->dest_host"]


}
```