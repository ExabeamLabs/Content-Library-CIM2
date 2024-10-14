#### Parser Content
```Java
{
Name = wiz-w-json-alert-trigger-success-ddosattack
 Vendor = Wiz
 Product = Wiz
 ExtractionType = json
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
 Conditions = [ """"category":"Detection"""", """DDoS Attack""", """"name":""", """"CLOUD_EVENTS"""" ]
 Fields = [
   """exa_json_path=$.event.timestamp,exa_field_name=time""",
   """exa_json_path=$.event.actor.IP,exa_field_name=src_ip""",
   """exa_json_path=$.event.actor.name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
   """exa_json_path=$.event.eventURL,exa_field_name=url""",
   """exa_regex=({app}wiz)"""
   """exa_json_path=$.event,exa_regex="matchedRules":.+ruleName:\s*({rule}[^,]+?)\s*",""",
   """exa_json_path=$.event.matchedRules,exa_regex=ruleId:\s*({rule_id}[^";,]+)""",
   """exa_json_path=$.event.subjectResource.region,exa_field_name=region""",
   """exa_json_path=$.event.subjectResource.account.id,exa_field_name=alert_id""",
 ]
 ParserVersion = v1.0.0
 DupFields = [ "rule->alert_name" ]


}
```