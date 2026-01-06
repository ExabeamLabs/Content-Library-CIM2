#### Parser Content
```Java
{
Name = "symantec-dlp-kv-email-send-success-emailsend-1"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS", "MMMM dd, yyyy hh:mm:ss a", "MMMM dd, yyyy h:mm:ss a" ]
Conditions = [
  """,endpoint_machine="""
  """,policy="""
  """,incident_snapshot="""
]
Fields = [
  """occuredOn=({time}\w+\s+\d+,\s+\d+\s+\d+:\d+:\d+\s+\w+)"""
  """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d\d\d[+-]\d\d:\d\d\s+({host}[\w\-.]+)"""
  """incident_id="*({alert_id}\d+)"""
  """policy="*({alert_name}[^",]+)("|,|\s*$)"""
  """protocol="*({protocol}[^",]+)("|,|\s*$)"""
  """policy="*({alert_type}[^",]+)("|,|\s*$)"""
  """recipients="*(?=[\w.]+@[\w.])?({email_recipients}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("|,|\s*$)"""
  """recipients="*(?=[\w.]+@[\w.])?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("|,|\s*$)"""
  """recipients="*(?=\w+:\/+)({target}[^",]+)("|,|\s*$)"""
  """sender="*(?=[\w.]+@[\w.])({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("|,|\s*$)"""
  """sender="*(?=[\w.]+@[\w.])({user}[\w\.\-\!\#\^\~]{1,40}\$?)("|,|\s*$)"""
  """severity="*({alert_severity}[^",]+)("|,|\s*$)"""
  """subject="*(?:N\/A|({email_subject}[^",]+))("|,|\s*$)"""
  """\sfile_name="*(?:N\/A|({file_name}[^",]+))\s*("|,|\s*$)"""
  """blocked="*({action}[^",]+)("|,|\s*$)"""
  """endpoint_machine="*(N\/A|({dest_host}[\w\-.]+))("|,|\s*$)"""
  """endpoint_user_name="*\s*(N\/A|(({domain}[^\\,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))("|,|\s*$)"""
  """endpoint_user_name="*\s*(N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s",@]+))"""
  """incident_snapshot=[^,]*?({alert_id}\d+),"""
  """machineIP="*(N\/A|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
]
SOAR {
  IncidentType = "dlp"
  NameTemplate = "Vontu DLP Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
        "dest_ip->ip_address"
        "dest_host->host_name"
      ]
    

}
```