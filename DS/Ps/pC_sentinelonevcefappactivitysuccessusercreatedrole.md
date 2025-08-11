#### Parser Content
```Java
{
Name = sentinelone-v-cef-app-activity-success-usercreatedrole
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|SentinelOne|Mgmt|""", """|User created role|""", """activityType=""", """notificationScope=""" ]
   Fields = ${SentinelOneParsersTemplates.sentinelone-vigilance-app-events.Fields}[
     """({operation}User created role)"""
   ]
 

}
```