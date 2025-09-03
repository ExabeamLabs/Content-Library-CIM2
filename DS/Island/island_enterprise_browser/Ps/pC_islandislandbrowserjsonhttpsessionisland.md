#### Parser Content
```Java
{
Name = "island-islandbrowser-json-http-session-island"
    Vendor = "Island"
    Product = "Island Enterprise Browser"
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ParserVersion = "v1.0.0"
    Conditions = [
        """"matchedDevicePosture":"""
        """userName"""
        """"urlWebCategories":"""
    ]
    Fields = [
        """exa_json_path=$.userId,exa_field_name=user_id"""
        """exa_json_path=$.deviceId,exa_field_name=device_id"""
        """exa_json_path=$.clientEventId,exa_field_name=event_id"""
        """exa_json_path=$.userName,exa_field_name=full_name"""
        """exa_json_path=$.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"""
        """exa_json_path=$.verdict,exa_field_name=result"""
        """exa_json_path=$.timestamp,exa_field_name=time"""
        """exa_json_path=$.country,exa_field_name=country"""
        """exa_json_path=$.details,exa_field_name=additional_info"""
        """exa_json_path=$.urlWebReputation,exa_field_name=reputation"""
        """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
        """exa_json_path=$.sourceIp,exa_field_name=src_ip"""
        """exa_json_path=$.region,exa_field_name=region"""
        """exa_json_path=$.publicIp,exa_field_name=dest_ip"""
        """exa_json_path=$.ruleName,exa_field_name=rule"""
        """exa_json_path=$.machineName,exa_field_name=dest_host"""
        """exa_json_path=$.ruleId,exa_field_name=rule_id"""
        """exa_json_path=$.tabId,exa_field_name=tab_title"""
        """exa_json_path=$.topLevelUrl,exa_field_name=url"""
        """exa_json_path=$.urlWebCategories,exa_field_name=categories"""
        """exa_json_path=$.matchedDevicePosture,exa_regex=[\\"\s]*domain[\\"\s]*:[\\"\s]*({web_domain}\w+\.\w+)"""
        """exa_json_path=$.matchedDevicePosture,exa_regex=[\\"\s]*computer_groups[\\"\s]*:[\\"\s]*({more_info}[^"\\,]+)"""
    ]


}
```