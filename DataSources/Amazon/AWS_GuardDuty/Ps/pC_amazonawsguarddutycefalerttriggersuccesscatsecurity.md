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
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s""",
    """\ssrc=({src_ip}[A-Fa-f\d:.]+?)\s""",
    """\sdst=({dest_ip}[A-Fa-f\d:.]+)""",
    """"privateIpAddress":"({dest_ip}[A-Fa-f\d:.]+)""",
    """\srequestClientApplication=({app}\S+)""",
    """\sdhost=({dest_host}\S+)""",
    """\ssuser=(|Anonymous|({user}[^=]+?))\s+(\w+=|$)""",
    """"type":"({alert_type}[^"]+?)"""",
    """"id":"({alert_id}[^"]+?)"""",
    """"title":"({alert_name}[^"]+?)"""",
    """"severity":"?({alert_severity}[^",]+)"?,""",
    """"service".*?"action".*?"portProbeAction".*?"portProbeDetails".*?"localPortDetails".*?"port":"({dest_port}\d+)"""",
    """"service".*?"action".*?"networkConnectionAction".*?"localPortDetails".*?"port":({dest_port}\d+)"""
    """"service".*?"action".*?"networkConnectionAction".*?"remotePortDetails".*?"port":"({src_port}\d+)"""",
    """"service".*?"action".*?"networkConnectionAction.*?"({result}blocked":"(false|true))""",
    """\smsg=({additional_info}.+?)(\s+\w+=|\s*$)""",
    """"tags":[^\]]+?\{"key":"Username","value":"({email_address}[^@"]+@[^\."]+\.[^"]+)""""
    ]


}
```