#### Parser Content
```Java
{
Name = amazon-awsguardduty-cef-alert-trigger-success-catsecurity
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = AWS GuardDuty
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """dproc=GuardDuty""", """cat=security-alert""", """destinationServiceName =AWS""" ]
  Fields = [
    """"createdAt":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\s""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"privateIpAddress":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\srequestClientApplication=({app}\S+)""",
    """\sdhost=({dest_host}\S+)""",
    """\ssuser=(|Anonymous|({user}[^=]+?))\s+(\w+=|$)""",
    """"type":"({alert_type}[^":]+?):({alert_name}[^"]+)"""",
    """"id":"({alert_id}[^"]+?)"""",
    """"title":"({event_name}[^"]+?)"""",
    """"severity":"?({alert_severity}[^",]+)"?,""",
    """"service".*?"action".*?"portProbeAction".*?"portProbeDetails".*?"localPortDetails".*?"port":"({dest_port}\d+)"""",
    """"service".*?"action".*?"networkConnectionAction".*?"localPortDetails".*?"port":({dest_port}\d+)"""
    """"service".*?"action".*?"networkConnectionAction".*?"remotePortDetails".*?"port":"({src_port}\d+)"""",
    """"service".*?"action".*?"networkConnectionAction.*?({result}"blocked":"*(false|true))""",
    """\smsg=({additional_info}.+?)(\s+\w+=|\s*$)""",
    """"tags":[^\]]+?\{"key":"Username","value":"({email_address}[^@"]+@[^\."]+\.[^"]+)""""
    ]


}
```