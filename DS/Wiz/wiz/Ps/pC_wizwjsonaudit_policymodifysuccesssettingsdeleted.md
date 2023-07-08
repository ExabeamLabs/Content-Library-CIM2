#### Parser Content
```Java
{
Name = wiz-w-json-audit_policy-modify-success-settingsdeleted
 Vendor = Wiz
 Product = Wiz
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
 Conditions = [ """"category":"Delete"""", """Diagnostic settings deleted""", """"name":""", """"CLOUD_EVENTS"""" ]
 Fields = [
   """"timestamp":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,7}Z)"""
   """"IP":"({src_ip}[a-fA-F\d.:]+)"""
   """actor":.*?"name":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))""""
   """"eventURL":"({url}[^"]+)"""
   """({app}wiz)"""
   """ruleName:\s*({rule}[^,]+?)\s*","""
   """"ruleId:\s*({rule_id}[^";,]+)""",
   """"region":"({region}[^"]+)""""
 ]
 ParserVersion = v1.0.0


}
```