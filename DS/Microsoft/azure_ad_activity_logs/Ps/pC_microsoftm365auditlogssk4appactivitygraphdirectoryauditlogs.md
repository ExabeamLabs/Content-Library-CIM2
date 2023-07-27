#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-sk4-app-activity-graphdirectoryauditlogs
 ParserVersion = v1.0.0
 Vendor = Microsoft
 Product = Azure AD Activity Logs
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 Conditions = [ """"src-application-name":"Office 365"""", """"src-endpoint":"Graph Directory Audit logs"""", """event-name":"audit-event""" ]
 Fields =[
   """"+time"+:"+({time}[^"]+)""",
   """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)\s+[^\s]+\s+""",
   """"+event-name"+:"+({event_name}[^"]+)""",
   """activityDisplayName":"({operation}[^"]+)""",
   """"displayName":"({email_address}[^@"]+@[^."]+\.[^"]+)","type":"User"""",
   """"+userPrincipalName"+:"+(({email_address}[^@"]+@[^"]+)|({user_id}[^"]+))""",
   """user":"({user}[\w\.\-]{1,40}\$?)""",
   """"type":"application","name":"({app}[^"]+)""",
   """"+application-action"+:"+({operation}[^"]+)""",
   """"+application-action".+?status"+.+?code":"+({result}[^"]+)""",
   """"+src-endpoint"+:"+({endpoint}[^"]+)""",
   """"+src-account-name"+:"+({account}[^"]+)""",
 ]


}
```