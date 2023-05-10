#### Parser Content
```Java
{
Name = google-workspace-sk4-app-activity-success-groups
  ParserVersion = v1.0.0
  Conditions = [ """destinationServiceName =Google Apps""", """"applicationName":"groups"""", """"uniqueQualifier":""" ]

cef-google-app-activity = {
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s""",
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"profileId":"({user_id}\d+)""",
    """"actor":\{[^=]*?"email":"({email_address}[^\s@"]+@({email_domain}[^\s@"]+))"""",
    """"events":\[\{[^\[\]\{\}]*"name"\s*:\s*"({operation}[^"]+)"""",
    """"name":"event_id","value":"({additional_info}[^"]+)"""",
    """"name":"EMAIL_LOG_SEARCH_RECIPIENT","value":"(unknown|({object}[^"]+))"""",
    """"name":"EMAIL_LOG_SEARCH_MSG_ID","value":"<?(unknown|({object}[^"]+?))>?"""",
    """"applicationName":"({app}[^"]+)"""",
    """"name":"app_name","value":"(unknown|({app}[^"]+?))\s*"""",
    """"name":"notification_type","value":"(unknown|({object}[^"]+))"""",
    """"name":"user_agent","value":"(unknown|({object}[^"]+))"""",
    """"name":"USER_EMAIL","value":"({object}[^"]+)"""",
    """"name":"calendar_id","value":"({object}[^"]+)"""",
    """"name":"target_calendar_id","value":"({object}[^"]+)"""",
    """"name":"group_email","value":"({object}[^"]+)"""",
    """"name":"status","value":"({object}[^"]+)"""",
    """"name":"client_id","value":"({object}[^"]+)"""",
    """"id":\{({additional_info}[^\}]+)\}"""
  
}
```