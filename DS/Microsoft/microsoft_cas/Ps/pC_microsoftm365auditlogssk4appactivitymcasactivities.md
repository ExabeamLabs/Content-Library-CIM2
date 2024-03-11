#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-sk4-app-activity-mcasactivities
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft CAS
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [  """"src-application-name":"Office 365"""", """"src-endpoint":"mcas-activities"""", """event-name":"audit-event""" ]
  Fields = [
     """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)\s+[^\s]+\s+""",
     """EventName":"({event_name}[^"]+)""",
     """EventId":({event_code}\d+)""",
     """"userName":"(({email_address}[^@"]+@[^@"]+)|({user_id}[\w-]+?))"""",
     """appName":"({app}[^"]+)""",
     """src-ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"location"[^}]+?city":"({location_city}[^",]+)""",
     """"location"[^}]+?countryCode":"({location_country}[^",]+)""",
     """"location"[^}]+?region":"({region}[^",]+)""",
     """activityResult":[^}]+?"isSuccess":({result}(?i)(true|false))""",
     """"application-action":"({operation}[^"]+)""",
     """"src-endpoint":"({endpoint}[^"]+)""",
     """"src-account-name":"({account}[^"]+)""",
     """application-msg":"({additional_info}[^"]+?)\s*",""",
     """collected":[^}]+?"resourceProvider":"({resource}[^"]+)""",
 ]


}
```