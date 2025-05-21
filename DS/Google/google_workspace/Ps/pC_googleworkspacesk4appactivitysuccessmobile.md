#### Parser Content
```Java
{
Name = google-workspace-sk4-app-activity-success-mobile
  ParserVersion = v1.0.0
  Conditions = [ """"kind"""", """"applicationName":"mobile"""", """"uniqueQualifier":""" ]
  Fields = ${GoogleParsersTemplates.cef-google-app-activity.Fields} [
  """"name":"OS_VERSION","value":"({os_version}[^"]+)""""
  ]

cef-google-app-activity = {
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s""",
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"profileId":"({user_id}\d+)""",
    """suser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+[\w=]+""",
    """"actor"\s*:\s*\{[^=]*?"email"\s*:\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
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
    """msg=({more_info}[^=]+)\s+\w+="""
    """"name":"ROLE_NAME","value":"({role_name}[^",\}]+)"""
    """"name":"PRIVILEGE_NAME","value":"({privileges}[^",\}]+)"""
    """"etag":"({tag}[^,]+)","""
    """"customerId":"({resource_id}[^"]+)""""
  ]
  DupFields = [ "operation->event_name" 
}
```