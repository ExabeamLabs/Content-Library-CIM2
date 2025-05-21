#### Parser Content
```Java
{
Name = symantec-dlp-cef-alert-trigger-success-contentsecurity
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Vontu|Monitor""", """catdt=Content Security""" ]
  Fields = [
    """([^\|]*\|){5}({alert_name}[^\|]+)""",
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\WeventId=({alert_id}\d+)""",
    """\Wmsg=({alert_type}.+?)\s*(\w+=|$)""",
    """\WdeviceSeverity=({alert_severity}\d+)""",
    """\WsourceDnsDomain=({web_domain}.+?)\s*(\w+=|$)""",
    """\Wcs1=(?:({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}\w+(?:\s+\w+)+))(\s+\w+=|\s*$)""",
    """\Wsuser=(?:N\/A|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({email_address}[^\s@]+@[^\s@]+))""",
    """\Wsuser=\w+:\/+({domain}[^\/\\=]+)[\\\/]+(?:({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}\w+(?:\s+\w+)+))(\s+\w+=|\s*$)""",
    """\WdestinationDnsDomain=({web_domain}.+?)\s*(\w+=|$)""",
    """\Wduser=(?:N\/A|({target}.+?))\s*(\w+=|$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wshost=(?:N\/A|({src_host}.+?))\s*(\w+=|$)""",
    """\Wfname=(?:N\/A|({file_name}.+?))\s*(\w+=|$)""",
    """\Wcs2=(None|({action}.+?))(\s+\w+=|\s*$)""",
    """\Wrequest=(unknown|N/A|({target}.+?))(\s+\w+=|\s*$)""",
    """\Wapp=(|({protocol}.+?))(\s+\w+=|\s*$)""",
    """\Wcs4=(|({email_subject}.+?))(\s+\w+=|\s*$)""",
  ]
  DupFields = ["target->recipients"]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_severity->sourceSeverity", "host->dlpDeviceName", "file_name->dlpFileName", "alert_type->dlpActionTaken"]
    NameTemplate = """Vontu DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```