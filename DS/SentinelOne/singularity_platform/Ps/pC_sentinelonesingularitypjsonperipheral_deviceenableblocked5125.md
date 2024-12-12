#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-peripheral_device-enable-blocked-5125"
Vendor = "SentinelOne"
Product = "Singularity Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
ExtractionType = json
Conditions = [
""""ruleName":"""
""""activityType":5125,"""
""""ruleid":"""
""""eventType":"blocked""""
]
Fields = [
"""exa_json_path=$.createdAt,exa_field_name=time""",
"""exa_json_path=$..ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$..creator,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?))|({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$"""
"""exa_json_path=$..ruleName,exa_field_name=rule""",
"""exa_json_path=$..eventId,exa_field_name=alert_id""",
"""exa_json_path=$..eventType,exa_field_name=operation""",
"""exa_json_path=$.primaryDescription,exa_field_name=additional_info""",
"""exa_json_path=$..osType,exa_field_name=os""",
"""exa_json_path=$.activityType,exa_field_name=event_code""",
"""exa_json_path=$.accountId,exa_field_name=account_id""",
"""exa_json_path=$.accountName,exa_field_name=account_name""",
"""exa_json_path=$..deviceName,exa_field_name=device_name""",
"""exa_json_path=$..interface,exa_field_name=interface""",
"""exa_json_path=$..bluetoothAddress,exa_field_name=src_mac"""
]
ParserVersion = "v1.0.0"


}
```