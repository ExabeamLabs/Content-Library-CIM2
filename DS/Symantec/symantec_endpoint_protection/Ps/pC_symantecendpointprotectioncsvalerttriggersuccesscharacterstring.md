#### Parser Content
```Java
{
Name = symantec-endpointprotection-csv-alert-trigger-success-characterstring
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""CIDS 特征字符串""", """Intrusion ID:"""]
Fields = [
    """本地:\s*({dest_ip}[a-fA-F:\.\d]+),本地:\s*(?:0+|({dest_host}[^,]+)).*?,入站,""",
    """远程:\s*({src_ip}[a-fA-F:\.\d]+),远程:\s*(?:0+|({src_host}[^,]+)).*?,入站,""",
    """本地:\s*({src_ip}[a-fA-F:\.\d]+),本地:\s*(?:0+|({src_host}[^,]+)).*?,出站,""",
    """远程:\s*({dest_ip}[a-fA-F:\.\d]+),远程:\s*(?:0+|({dest_host}[^,]+)).*?,出站,""",
    """开始:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """用户:\s*(({full_name}[^,\s]+(\s+[^,\s]+)+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
    """域:(?:\s+|\s*({domain}[^,]+)),""",
    """应用程序:(?:\s+|\s*({process_path}({process_dir}(?:[^,]+)?[\\\/])?({process_name}[^\\\/,]+?))),""",
    """CIDS 特征 ID:\s*({alert_name}\d+),""",
    """Intrusion ID:\s*({alert_id}\d+),""",
    """CIDS 特征字符串:\s*({alert_type}[^:,]+),""",
    """CIDS 特征字符串:\s*({alert_name}[^:,]+),""",
    """CIDS 特征字符串:\s*({alert_type}[^:,]+):\s*({alert_name}[^,]+)""",
    """入侵 URL:(?:\s+|\s*({malware_url}[^,]+)),""",
    """CIDS 特征 ID:\s*({alert_id}\d+),""",
    """\w{3}\s+\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\.-]+)\s""",
    """\s*({host}[^,]+),SHA-256:""",
  ]
  DupFields = ["directory->process_dir"]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_id->sourceId", "src_ip->malwareVictimHost", "malware_url->malwareAttackerUrl", "dest_ip->malwareAttackerIp", "alert_type->malwareCategory"]
    NameTemplate = """Symantec Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```