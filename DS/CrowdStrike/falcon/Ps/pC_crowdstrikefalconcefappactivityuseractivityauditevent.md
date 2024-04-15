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
Fields = [
""""eventCreationTime":\s*({time}\d{10})"""
""""UserId":\s*"({email_address}[^"@]+@[^"@]+)""""
""""UserId":\s*"(Crowdstrike|CrowdStrike|({email_address}[^@"]+@[^\."]+\.[^"]+)|({user_id}[^"@]+))"""",
""""assigned_to_uid".+?"ValueString":"({email_address}[^@"]+@[^\."]+\.[^"]+)""",
""""UserIp":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""ServiceName":\s*"({resource}[^"]+)"""
"""({app}CrowdStrike)"""
""""OperationName":\s*"({operation}[^",]+)"""
""""AuditKeyValues":\[({additional_info}.+?)\]"""
""""AuditKeyValues":[^\]]+?((_name")|(_id")|(Id"+)),"ValueString":"({object}[^"]+?)\s*"(,|\})"""
""""aid":\s*"({aid}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```