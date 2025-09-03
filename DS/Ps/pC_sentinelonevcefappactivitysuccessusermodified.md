#### Parser Content
```Java
{
Name = sentinelone-v-cef-app-activity-success-usermodified
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|SentinelOne|Mgmt|""", """|Administrative information - User Modified|""", """activityType=""", """notificationScope=""" ]
   Fields = ${SentinelOneParsersTemplates.sentinelone-vigilance-app-events.Fields}[
     """({operation}User Modified)"""
   ]
 

}
```