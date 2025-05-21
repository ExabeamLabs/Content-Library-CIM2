#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-app-activity-useractivityauditevent"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""eventType":"""
""""UserActivityAuditEvent""""
""""OperationName":"""
]
ExtractionType = json
Fields = [
""""eventCreationTime":\s*({time}\d{10})"""
""""UserId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
""""UserId":\s*"(Crowdstrike|CrowdStrike|({email_address}[^@"]+@[^\."]+\.[^"]+)|({user_id}[^"@]+))"""",
""""assigned_to_uid".+?"ValueString":"({email_address}[^@"]+@[^\."]+\.[^"]+)""",
""""UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""ServiceName":\s*"({resource}[^"]+)"""
"""({app}CrowdStrike)"""
""""OperationName":\s*"({operation}[^",]+)"""
""""AuditKeyValues":\[({additional_info}.+?)\]"""
""""AuditKeyValues":[^\]]+?(,|\}),[^\]]+?"ValueString":"({object}[^"]+?)\s*"(,|\})"""
""""AuditKeyValues":[^\]]+?((_name")|(_id")|(Id"+)),"ValueString":"({object}[^"]+?)\s*"(,|\})"""
""""aid":\s*"({aid}[^"]+)"""
""""cid":"({cid}[^"]+)""""
""""customerIDString":"({cid}[^"]+)""""
"""exa_json_path=$..cid,exa_field_name=cid""",
"""exa_json_path=$..customerIDString,exa_field_name=cid""",
"""exa_json_path=$..eventCreationTime,exa_field_name=time""",
"""exa_regex="UserId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
"""exa_regex="UserId":\s*"(Crowdstrike|CrowdStrike|({email_address}[^@"]+@[^\."]+\.[^"]+)|({user_id}[^"@]+))"""",
"""exa_json_path=$..UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$..ServiceName,exa_field_name=resource""",
"""exa_regex=({app}CrowdStrike)"""
"""exa_json_path=$..OperationName,exa_field_name=operation""",
"""exa_json_path=$..AuditKeyValues[*],exa_field_name=additional_info"""
"""exa_json_path=$..AuditKeyValues[1].ValueString,exa_field_name=object"""
]
ParserVersion = "v1.0.0"


}
```