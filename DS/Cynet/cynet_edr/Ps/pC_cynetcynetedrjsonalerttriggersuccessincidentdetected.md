#### Parser Content
```Java
{
Name = cynet-cynetedr-json-alert-trigger-success-incidentdetected
       Vendor = Cynet
       Product = Cynet EDR
       TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
       Conditions = [ """Alert Name:""", """Cynet""", """Severity""" , """Incident detected on:""" ]
       ExtractionType = json
       ParserVersion = v1.0.0
       Fields = [
          """exa_json_path=$.NetworkRisk,exa_field_name=risk_level""",
          """exa_regex=Hostname:"Hostname:\s*({host}[^\s\\]+)((?-i)\\+[rnt])+?Host IP:\s*\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
          """exa_regex=Process Path:\s*({process_path}\w+:[^:]+?)[(?i)\\+(rtn)+]*\s*Process Params:"""
          """exa_regex=OS Version:\s({os}[^"\\]+)"""
          """exa_regex=Alert Name:\s*({alert_name}[^"\\]+)"""
          """exa_regex=SHA256:\s*({hash_sha256}[^\\"]+)"""
          """exa_regex=User SID:\s({user_sid}[^\s\\]+)"""
         """exa_json_path=$.Sha256,exa_field_name=hash_sha256""",
         """exa_json_path=$.HostName,exa_field_name=host""",
         """exa_json_path=$.UserName,exa_regex="UserName":"(({domain}[^\\]+)[\\]+)?({user}[\w\.\-]{1,40}\$?)"""
         """exa_json_path=$.Severity,exa_field_name=alert_severity""",
         """exa_json_path=$.Subject,exa_field_name=alert_subject""",
         """exa_json_path=$.StringIP,exa_field_name=alert_source""",
         """exa_json_path=$.LastSeen,exa_field_name=time"""
      ]
    

}
```