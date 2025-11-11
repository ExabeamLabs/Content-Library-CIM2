#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-alert-trigger-success-scanningyourcomputer
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CIDS Signature string""", """Somebody is scanning your computer""" ]
  Fields = [
		"""\w+\s+\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\.-]+)\s"""
		"""Local:\s*({dest_ip}[a-fA-F:\.\d]+),Local:\s*(?:0+|({dest_host}[^,]+)),([^,]*,){3}Inbound,({protocol}\w+),([^,]*,){8}Local Port ({dest_port}\d+),"""
		"""Remote:\s*({src_ip}[a-fA-F:\.\d]+),Remote:\s*(?:0+|({src_host}[^,]+)),Inbound,"""
		"""Local:\s*({src_ip}[a-fA-F:\.\d]+),Local:\s*(?:0+|({src_host}[^,]+)),([^,]*,){3}Outbound,({protocol}\w+),"""
		"""Remote:\s*({dest_ip}[a-fA-F:\.\d]+),Remote:\s*(?:0+|({dest_host}[^,]+)),Outbound,([^,]*,){10}Remote Port ({dest_port}\d+),"""
		"""Begin:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
		"""User:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?),"""
		"""Domain:\s*({domain}[^,]+),"""
		"""({alert_name}Somebody is scanning your computer)"""
		""""({additional_info}SymantecServer[^"]+)"""
		"""({alert_type}Somebody is scanning your computer)"""
  ]
  SOAR {
    IncidentType = "generic"
    NameTemplate = """Symantec Network Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```