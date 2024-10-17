#### Parser Content
```Java
{
Name = symantec-dlp-str-email-receive-incident
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""Vontu Incident: """,
"""^^"""
  ]
  Fields = [
    """\s({host}[\w\.-]+)\s+Vontu Incident: """,
    """Vontu Incident:\s+({alert_name}.+?)\s*\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^)({alert_id}\d+)\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){2}(N\/A|({email_subject}.+?))\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){3}(N\/A|({alert_severity}.+?))\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){6}(N\/A|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){6}(N\/A|({os}[^:\^]+):\/\/({domain}[^\/\^]+)\/({user}[\w\.\-\!\#\^\~]{1,40}\$?))\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){6}(N\/A|({src_ip}(\d{1,3}\.){3}\d{1,3}))\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){7}(N\/A|({email_recipients}((?!\w+:\/\/)[^@\s]+@\S+?)(,[^@\s]+@\S+?)*))\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){7}(N\/A|({target}([^\^]|\^[^\^])+?))\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){7}(N\/A|\s*({url}(\w+:\/+)?({web_domain}[^\\\/]+)[^\s]+))(\/\S+?)?\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){8}(N\/A|({action}.+?))\^\^""",
    """Vontu Incident:\s+(([^\^]|\^[^\^])+?\^\^){13}(N\/A|({alert_type}.+?))\^\^""",
    """({direction}o)""",
  ]
  DupFields = [ "email_address->original_user" ]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_severity->sourceSeverity", "src_ip->dlpDeviceName", "action->dlpActionTaken"]
    NameTemplate = """Vontu DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```