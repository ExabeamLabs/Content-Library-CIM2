#### Parser Content
```Java
{
Name = logmein-ra-kv-endpoint-logout-success-policyname
  Vendor = LogMeIn
  Product = RemotelyAnywhere
  TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
  Conditions = [ """"Windows_Remotely_Anywhere_Policy""", """ POLICY_NAME: """, """RA_LogOff""" ]
  Fields = [
    """EVENT_DT:\s"+({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d)"""",
    """\sHOSTADDR:\s"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """\sSession\s-\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?:(({domain}\w+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s-\sLogged out.""",
    """\sDESCRIPTION:\s"+({description}[^"]+)"""",
    """\sRULE_NAME: "*({rule}[^"]+)"""",
    """\sPOLICY_NAME:\s+"+({policy_name}[^"]+)"+\s""",
    """EVENT_ID:\s+"+({alert_id}[^"]+)"+\s""",
    """\sEVENT_TYPE_D:\s+"+({event_name}[^"]+)"+\s""",
    """\sHOSTNAME:\s+"+({host}[^"]+)"+\s""",
    """\sOSTYPE_D:\s+"+({os}[^"]+)"+\s""",
    """\sEVENT_SEVERITY_D:\s+"+({alert_severity}[^"]+)"+\s""",
    """\sDOMAIN_NAME:\s+"+(unknown|null|({domain}[^"]+))"+\s""",
    """\sUSER_NAME:\s+"+(unknown|null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+\s""",
    """\sSESSION_ID:\s+"+(unknown|null|({session_id}[^"]+))"+\s""",
    """\sPROCESS_NAME:\s+"+(unknown|null|({process_name}[^"]+))"+\s""",
    """\sRESOURCE_NAME:\s+"+(unknown|null|({resource}[^"]+))"+\s""",
    """\sTARGET_INFO:\s+"+(unknown|null|({resource}[^"]+))"+\s""",
    """\sUSER_NAME:\s+"+(unknown|null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+\s"""
  ]
  ParserVersion = "v1.0.0"


}
```