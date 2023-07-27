#### Parser Content
```Java
{
Name = wiz-w-json-alert-trigger-success-ddosattack
 Vendor = Wiz
 Product = Wiz
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
 Conditions = [ """"category":"Detection"""", """DDoS Attack""", """"name":""", """"CLOUD_EVENTS"""" ]
 Fields = [
   """"timestamp":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,7}Z)"""
   """"IP":"({src_ip}[a-fA-F\d.:]+)"""
   """actor":.*?"name":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""""
   """"eventURL":"({url}[^"]+)"""
   """({app}wiz)"""
   """ruleName:\s*({rule}[^,]+)","""
   """"ruleId:\s*({rule_id}[^";,]+)""",
   """"region":"({region}[^"]+)""""
   """"id":"({alert_id}[^"]+)"""
 ]
 ParserVersion = v1.0.0
 DupFields = [ "rule->alert_name" ]


}
```