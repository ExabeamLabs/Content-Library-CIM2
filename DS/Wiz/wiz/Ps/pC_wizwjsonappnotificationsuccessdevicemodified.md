#### Parser Content
```Java
{
Name = wiz-w-json-app-notification-success-devicemodified
 Vendor = Wiz
 Product = Wiz
 ExtractionType = json
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
 Conditions = [ """"category":"Delete"""", """Virtual network device modified""", """"name":""", """"CLOUD_EVENTS"""" ]
 Fields = [
   """exa_json_path=$.event.timestamp,exa_field_name=time""",
   """exa_json_path=$.event.actor.IP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
   """exa_json_path=$.event.actor.name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
   """exa_json_path=$.event.eventURL,exa_field_name=url""",
   """exa_regex=({app}wiz)""",
   """exa_json_path=$.event,exa_regex="matchedRules":.+ruleName:\s*({rule}[^,]+?)\s*",""",
   """exa_json_path=$.event.matchedRules,exa_regex=ruleId:\s*({rule_id}[^";,]+)""",
   """exa_json_path=$.event.subjectResource.region,exa_field_name=region"""
 ]
 ParserVersion = v1.0.0


}
```