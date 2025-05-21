#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-alert-trigger-success-denialofservice
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CIDS Signature ID""", """Denial of Service""" ]
  Fields = [
		"""\w+\s+\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\.-]+)\s"""
		"""Local:\s*({dest_ip}[a-fA-F:\.\d]+),Local:\s*(?:0+|({dest_host}[^,]+)),([^,]*,){3}Inbound,({protocol}\w+),([^,]*,){9}Local Port ({dest_port}\d+),"""
		"""Remote:\s*({src_ip}[a-fA-F:\.\d]+),Remote:\s*(?:0+|({src_host}[^,]+)),Inbound,"""
		"""Local:\s*({src_ip}[a-fA-F:\.\d]+),Local:\s*(?:0+|({src_host}[^,]+)),([^,]*,){3}Outbound,({protocol}\w+),"""
		"""Remote:\s*({dest_ip}[a-fA-F:\.\d]+),Remote:\s*(?:0+|({dest_host}[^,]+)),Outbound,([^,]*,){10}Remote Port ({dest_port}\d+),"""
		"""Remote Host Name:\s*(|({src_host}[\w\-.]+)),(Remote Host IP:\s*(?:0+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),)?.*?,Inbound,({protocol}\w+),"""
		"""Remote Host Name:\s*(|({dest_host}[\w\-.]+),),(Remote Host IP:\s*(?:0+|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?))?.*?,Outbound,({protocol}\w+),"""
		"""Local Host IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.*?,Outbound,({protocol}\w+),"""
		"""Local Host IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?.*?,Inbound,({protocol}\w+),"""
		"""Begin:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
		"""User( Name)?:\s*(none|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
		"""Domain( Name)?:\s*({domain}[^,\s]+),"""
		"""SymantecServer:\s*.*?({alert_name}Denial of Service[^:]+?)\s*Description:"""
		"""\W\s+Description:\s*({additional_info}[^\.:]+)"""

  ]
  DupFields = [ "alert_name->alert_type" ]
  SOAR {
    IncidentType = "generic"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->description"]
    NameTemplate = """Symantec Network Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```