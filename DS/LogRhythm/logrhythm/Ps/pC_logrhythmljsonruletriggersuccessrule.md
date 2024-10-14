#### Parser Content
```Java
{
Name = logrhythm-l-json-rule-trigger-success-rule
    ParserVersion = "v1.0.0"
    Vendor = LogRhythm
    Product = LogRhythm
    ExtractionType = json
    TimeFormat = "epoch"
    trigger_timeFormat = ["epoch_sec", "epoch"]
    Conditions = [""""cmsCanonicalId":""", """"ruleElements":""", """"messageIds":""", """"description":"""]
    Fields = [
      """exa_json_path=$.description,exa_field_name=rule_description""",
      """exa_json_path=$.name,exa_field_name=rule""",
      """exa_json_path=$.timestamp,exa_field_name=trigger_time"""
    ]
    DupFields = [ "rule_description->rule_reason", "trigger_time->time" ]


}
```