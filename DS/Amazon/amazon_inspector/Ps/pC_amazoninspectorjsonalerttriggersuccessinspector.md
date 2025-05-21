#### Parser Content
```Java
{
Name = amazon-inspector-json-alert-trigger-success-inspector
   Vendor = Amazon
   Product = Amazon Inspector
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
   ExtractionType = json
   Conditions = [ """"source":"aws.inspector2"""", """"title":"""", """"inspectorScoreDetails":""" ]
   Fields = [
     """exa_json_path=$.time,exa_field_name=time""",
     """exa_regex="ipV4Addresses":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """exa_regex="ipV6Addresses":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """exa_json_path=$.detail.title,exa_field_name=alert_name""",
     """exa_json_path=$.detail.type,exa_field_name=alert_type""",
     """exa_json_path=$.detail.severity,exa_field_name=alert_severity""",
     """exa_json_path=$.detail.awsAccountId,exa_field_name=account_id""",
     """exa_json_path=$.detail.description,exa_field_name=additional_info""",
     """exa_json_path=$.detail.status,exa_field_name=alert_status""",
     """exa_json_path=$.id,exa_field_name=alert_id""",
     """exa_json_path=$.account,exa_field_name=aws_account""",
     """exa_json_path=$.source,exa_field_name=alert_source""",
     """exa_json_path=$.detail-type,exa_field_name=alert_source""",
     """exa_json_path=$.resources[0],exa_field_name=resource_id""",
     """exa_json_path=$..sourceUrl,exa_field_name=url""",
     """exa_json_path=$..tags.Name,exa_field_name=tag""",
     """exa_json_path=$..resources.region,exa_field_name=region""",
     """exa_json_path=$..resources.type,exa_field_name=resource_type"""
   ]
   ParserVersion = v1.0.0


}
```