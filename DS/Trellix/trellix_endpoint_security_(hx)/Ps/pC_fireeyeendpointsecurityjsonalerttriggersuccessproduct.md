#### Parser Content
```Java
{
Name = "fireeye-endpointsecurity-json-alert-trigger-success-product"
Conditions = [
"""msg"""
"""alert"""
"""product"""
""""HX""""
]
ExtractionType = json
ParserVersion = "v1.0.0"

fireeye-networksecurity-nx-events.Fields}[
      """exa_json_path=$.http.url,exa_field_name=file_path""",
      """exa_json_path=$.fileinfo.filename,exa_field_name=file_path""",
      """exa_json_path=$.fileinfo.filename,exa_regex=({file_path}((|({file_dir}[^"]*?)[\\\/]+))?({file_name}[^"\\\/]+?(\.({file_ext}[^"\/\\\.]+))?))("|$)""",
      """exa_json_path=$.fileinfo.state,exa_field_name=state""",
      """exa_json_path=$.fileinfo.md5,exa_field_name=hash_md5""",
      """exa_json_path=$.fileinfo.size,exa_field_name=bytes""",
      """exa_json_path=$.fileinfo.file_id,exa_field_name=file_id""",
      """exa_json_path=$.http.http_method,exa_field_name=method""",
      """exa_json_path=$.http.status,exa_field_name=http_response_code""",
      """exa_json_path=$.http.http_user_agent,exa_field_name=user_agent""",
      """exa_json_path=$.http.protocol,exa_field_name=protocol""",
      """exa_json_path=$.http.hostname,exa_field_name=web_domain""",
      """exa_json_path=$.http.http_port,exa_field_name=dest_port""",
      """exa_json_path=$.http.http_content_type,exa_field_name=mime"""
    ]
	ParserVersion = "v1.0.0"
}

${FireEyeParsersTemplates.fireeye-networksecurity-nx-events}{
	Name = "fireeye-networksecurity-json-network-traffic-success-flow"
	Conditions = [ """"event_type":"flow"""", """"flow_id":""", """"flow":{""", """"bytes_toserver":""", """"bytes_toclient":""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
  	  """exa_json_path=$.flow.pkts_toserver,exa_field_name=packets_out""",
    	"""exa_json_path=$.flow.pkts_toclient,exa_field_name=packets_in""",
    	"""exa_json_path=$.flow.bytes_toserver,exa_field_name=bytes_out""",
    	"""exa_json_path=$.flow.bytes_toclient,exa_field_name=bytes_in""",
    	"""exa_json_path=$.flow.iface_toserver,exa_field_name=egress_interface""",
    	"""exa_json_path=$.flow.iface_toclient,exa_field_name=ingress_interface""",
    	"""exa_json_path=$.flow.reason,exa_field_name=result_reason"""
    ]
	ParserVersion = "v1.0.0"
}

${FireEyeParsersTemplates.fireeye-networksecurity-nx-events}{
	Name = "fireeye-networksecurity-json-http-session-success-http"
	Conditions = [ """"event_type":"http"""", """"flow_id":""", """"http":{""", """"http_method":"""", """"proto":""", """"iface":""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
  	  """exa_json_path=$.http.hostname,exa_field_name=web_domain""",
    	"""exa_json_path=$.http.http_port,exa_field_name=dest_port""",
    	"""exa_json_path=$.http.url,exa_field_name=uri_path""",
    	"""exa_json_path=$.http.http_content_type,exa_field_name=mime""",
    	"""exa_json_path=$.http.http_method,exa_field_name=method""",
    	"""exa_json_path=$.http.protocol,exa_field_name=protocol""",
    	"""exa_json_path=$.http.status,exa_field_name=http_response_code"""
    ]
	ParserVersion = "v1.0.0"
}

${FireEyeParsersTemplates.fireeye-networksecurity-nx-events}{
	Name = "fireeye-networksecurity-json-dns-response-success-dnsanswer"
	Conditions = [ """"event_type":"dns"""", """"flow_id":""", """"dns":{""", """"rcode":"""", """"rrname":"""", """"type":"answer"""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
  	  """exa_json_path=$.dns.id,exa_field_name=dns_query_id""",
    	"""exa_json_path=$.dns.rcode,exa_field_name=dns_response_code""",
    	"""exa_json_path=$.dns.rrname,exa_field_name=dns_response""",
    	"""exa_json_path=$.dns.rrtype,exa_field_name=dns_record_type"""
    ]
	ParserVersion = "v1.0.0"
}

${FireEyeParsersTemplates.fireeye-networksecurity-nx-events}{
	Name = "fireeye-networksecurity-json-dns-request-success-dnsquery"
	Conditions = [ """"event_type":"dns"""", """"flow_id":""", """"dns":{""", """"rrname":"""", """"type":"query"""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
  	  """exa_json_path=$.dns.id,exa_field_name=dns_query_id""",
    	"""exa_json_path=$.dns.rcode,exa_field_name=dns_response_code""",
    	"""exa_json_path=$.dns.rrname,exa_field_name=dns_query""",
    	"""exa_json_path=$.dns.rrtype,exa_field_name=dns_response_type"""
    ]
	ParserVersion = "v1.0.0"
}

${FireEyeParsersTemplates.fireeye-networksecurity-nx-events}{
	Name = "fireeye-networksecurity-json-network-traffic-success-smb2"
	Conditions = [ """"event_type":"smb2"""", """"flow_id":""", """"smb2":{""", """"command_str":"""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
    	"""exa_json_path=$.smb2.command_str,exa_field_name=command""",
    	"""exa_json_path=$.smb2.pid,exa_field_name=process_id""",
    	"""exa_json_path=$.smb2.sid,exa_field_name=session_id""",
    	"""exa_json_path=$.smb2.mid,exa_field_name=message_id""",
    	"""exa_regex="smb2":\{[^\}]+?"command_str":"(?i)({access}create|write|close|read)"[^}]+?"\w+":\{[^}]*?"fid":"({file_id}[^"]+)"""",
    	"""exa_regex="smb2":\{[^\}]+?"command_str":"(?i)({access}create|write|close|read)"[^}]+?"\w+":\{[^}]*?"filename":"({file_path}((|({file_dir}[^"]*?)[\\\/]+))?({file_name}[^"\\\/]+?(\.({file_ext}[^"\/\\\.]+))?))""""
    ]
	ParserVersion = "v1.0.0"
}

${FireEyeParsersTemplates.fireeye-networksecurity-nx-events}{
	Name = "fireeye-networksecurity-json-endpoint-login-success-krb5"
	Conditions = [ """"event_type":"krb5"""", """"flow_id":""", """"krb5":{""", """"request_type":"""", """realm"""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
    	"""exa_json_path=$.krb5.client[:1],exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    	"""exa_json_path=$.krb5.server_realm,exa_field_name=domain""",
    	"""exa_json_path=$.krb5.client_realm,exa_field_name=domain""",
    	"""exa_json_path=$.krb5.success,exa_field_name=result""",
    	"""exa_regex="krb5":\{[^\}]+?"server":\[[^\]]*?("\w+",)?"(cisfdata|({dest_host}[\w\-\.]+)(:\d+)?)"""",
    ]
	ParserVersion = "v1.0.0"
}

${FireEyeParsersTemplates.fireeye-networksecurity-nx-events}{
	Name = "fireeye-networksecurity-json-ssh-traffic-success-ssh"
	Conditions = [ """"event_type":"ssh"""", """"flow_id":""", """"ssh":{""", """"server":{""", """"client":{""", """"software_version":"""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
  	  """exa_json_path=$.ssh.server.software_version,exa_field_name=server_ssh_version""",
  	  """exa_json_path=$.ssh.client.software_version,exa_field_name=client_ssh_version"""
    ]
	ParserVersion = "v1.0.0"
}

${FireEyeParsersTemplates.fireeye-networksecurity-nx-events}{
	Name = "fireeye-networksecurity-json-network-traffic-success-modbus"
	Conditions = [ """"event_type":"modbus"""", """"flow_id":""", """"modbus":{""", """"transaction_id":""", """"function_code":"""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
  	  """exa_json_path=$.modbus.transaction_id,exa_field_name=server_ssh_version""",
  	  """exa_json_path=$.modbus.function_code,exa_field_name=operation""",
  	  """exa_json_path=$.modbus.function_category,exa_field_name=category""",
    ]
	ParserVersion = "v1.0.0"
}

${FireEyeParsersTemplates.fireeye-networksecurity-nx-events}{
	Name = "fireeye-networksecurity-json-radius-traffic-radius"
	Conditions = [ """"event_type":"radius"""", """"flow_id":""", """"radius":{""", """"iface":"""" ]
  	Fields = ${FireEyeParsersTemplates.fireeye-networksecurity-nx-events.Fields}[
  	  """exa_json_path=$.radius.reply.code,exa_field_name=result_code"""
  	  """exa_json_path=$.radius.request.code,exa_field_name=result_code"""
  	  """exa_json_path=$.radius.success,exa_field_name=result"""
    ]
	ParserVersion = "v1.0.0"
}

{
  Name = "fireeye-helix-json-alert-trigger-success-alerts"
  Vendor = "Trellix"
  Product = "Trellix Endpoint Security (HX)"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"event_type":""", """"resolution":"ALERT"""", """"source":""", """"md5values":""", """"agent":""", """"indicator":""", """"is_false_positive":false""" ]
  Fields = [
    """exa_json_path=$.indicator.name,exa_field_name=indicator""",
    """exa_json_path=$.indicator.category,exa_field_name=category""",
    """exa_json_path=$.agent._id,exa_field_name=agent_id""",
    """exa_json_path=$.md5values[0],exa_field_name=hash_md5""",
    """exa_json_path=$.event_at,exa_field_name=time""",
    """exa_json_path=$.url,exa_field_name=url""",
    """exa_json_path=$.source,exa_field_name=alert_source""",
    """exa_json_path=$.resolution,exa_field_name=result""",
    """exa_json_path=$.event_id,exa_field_name=event_id"""
    """exa_json_path=$.event_type,exa_field_name=alert_type"""
    """exa_json_path=$..infection.infection-type,exa_field_name=alert_type"""
    """exa_json_path=$..infection.infection-name,exa_field_name=alert_name"""
    """exa_json_path=$.indicator.display_name,exa_field_name=alert_name"""
    """exa_json_path=$..confidence-level,exa_field_name=alert_severity""",
    """exa_json_path=$..actor-process.path,exa_field_name=process_path"""
    """exa_json_path=$..user.domain,exa_field_name=domain"""
    """exa_json_path=$..user.username,exa_field_name=user"""
    """exa_json_path=$..sub-type,exa_field_name=subtype"""
    """exa_json_path=$..file-event.file-path,exa_field_name=file_path"""
    """exa_json_path=$..os-details.$.name,exa_field_name=os"""
    """exa_json_path=$..action.result,exa_field_name=result"""
    """exa_regex=eventReason":\s*"({operation}[^"]+)""""
    """exa_regex=fileName":\s*"({file_name}[^"]+)""""
    """exa_regex="id":"({process_id}process[^"]+)""""
    """exa_regex=processCmdLine":\s*"({process_command_line}[^"]+)""""
    """exa_regex=\Wprocess":\s*"({process_name}[^"]+)""""
    """exa_regex=\WprocessPath":\s*"(({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+(\.[a-zA-Z]+)))|({=process_dir}[^"]+))""""
    """exa_regex=(username|account_name)":\s*"(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """exa_regex=(filePath|file_path)":"({file_path}[^"]+)""""
    """exa_regex=fullPath":"({file_path}[^"]+)""""
    """exa_regex=(filePath|file_path).+?"name":"({file_name}[^"]+)""""
    """exa_regex=fileName":"({file_name}[^"]+)""""
    """exa_json_path=$..event_values[?(@.type == 'alert')].name,exa_field_name=alert_name"""
    """exa_json_path=$..event_values[?(@.type == 'alert')].alert_type,exa_field_name=alert_type"""
    """exa_json_path=$..event_values[?(@.type == 'alert')].description,exa_field_name=alert_description"""
    """exa_json_path=$..event_values[?(@.type == 'alert')].parameters.matched_rule,exa_field_name=rule"""
    """exa_json_path=$..event_values[?(@.type == 'eventlog')].extensions..categoryTechnique,exa_field_name=category"""
    """exa_json_path=$..event_values[?(@.type == 'process')].arguments,exa_field_name=process_command_line"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..Name,exa_field_name=rule"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..UUID,exa_field_name=rule_uid"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..Desc,exa_field_name=rule_description"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..Confidence,exa_field_name=alert_severity"""
    """exa_json_path=$..event_values[?(@.type == 'finding')].matched_rule..Mitre,exa_field_name=mitre_labels"""
    """exa_json_path=$..event_values[?(@.type == 'action')].name,exa_field_name=action"""
    """exa_json_path=$..event_values[?(@.type == 'event')].name,exa_field_name=event_name"""
  ]
  ParserVersion = "v1.0.0"
}

{
Vendor = "Trellix"
Product = "Trellix Endpoint Security (HX)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
"""exa_json_path=$.alert.event_values.processEvent/timestamp,exa_field_name=time""",
"""exa_json_path=$.alert._id,exa_field_name=alert_id""",
"""exa_json_path=$.alert.indicator.display_name,exa_field_name=event_name""",
"""exa_json_path=$.alert.indicator.display_name,exa_field_name=alert_name""",
"""exa_json_path=$.alert.host.hostname,exa_regex=^({src_host}[\w\-.]+)$""",
"""exa_json_path=$.alert.host.ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
"""exa_json_path=$.alert.host.agent_id,exa_field_name=agent_id""",
"""exa_json_path=$.alert.sysinfo.mac_address,exa_field_name=src_mac""",
"""exa_json_path=$.alert.event_values.processEvent/process,exa_field_name=process_name""",
"""exa_json_path=$.alert.event_values.processEvent/eventType,exa_field_name=event_category""",
"""exa_json_path=$.alert.event_values.processEvent/processPath,exa_field_name=process_path""",
"""exa_json_path=$.alert.event_values.processEvent/pid,exa_field_name=process_id""",
"""exa_json_path=$.alert.event_values.processEvent/parentPid,exa_field_name=parent_process_id""",
"""exa_json_path=$.alert.event_values.processEvent/parentProcess,exa_field_name=parent_process_name""",
"""exa_json_path=$.alert.event_values.processEvent/parentProcessPath,exa_field_name=parent_process_path""",
"""exa_json_path=$.alert.event_values.processEvent/md5,exa_field_name=hash_md5""",
"""exa_json_path=$.alert.event_values.processEvent/username,exa_regex=^(({domain}[^\\]+)\\+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
"""exa_json_path=$.alert.event_values.processEvent/processCmdLine,exa_field_name=process_command_line""",
"""exa_json_path=$.alert.uuid,exa_field_name=user_uid""",
"""exa_json_path=$.alert.host.domain,exa_field_name=domain""",
"""exa_json_path=$.version,exa_field_name=version""",
"""exa_json_path=$.alert.event_type,exa_field_name=alert_type""",
"""exa_json_path=$.appliance,exa_regex=^({host}[\w\-.]+)$"""
]
Name = "fireeye-endpointsecurity-json-alert-trigger-success-product"
Conditions = [
"""msg"""
"""alert"""
"""product"""
""""HX""""
]
ExtractionType = json
ParserVersion = "v1.0.0"
}

{
Name = "fireeye-networksecurity-csv-alert-trigger-success-webmps"
Vendor = "Trellix"
Product = "Trellix Web MPS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""CSV:0:FireEye:Web MPS"""
]
Fields = [
""",occurred=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""dvchost=({host}[^,]+)"""
"""alertid=({alert_id}\d+)"""
"""alertType=({alert_type}[^,]+)"""
"""alertType=({alert_name}[^,]+)"""
"""sev=({alert_severity}[^,]+)"""
"""sname=({alert_name}[^,]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""shost=({src_host}[^,]+)"""
"""cnchost=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^,]+))"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""dhost=({dest_host}[^,]+)"""
"""~+User-Agent:\s+({user_agent}.+?)::"""
"""mwurl=({malware_url}[^,]+)"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_name->malwareName"
"alert_type->malwareCategory"
"alert_severity->sourceSeverity"
"src_ip->malwareVictimHost"
"malware_url->malwareAttackerUrl"
"dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "FireEye Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
"""src_ip->ip_address"""
"""src_host->host_name"""
      ]
    }
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
"""dest_ip->ip_address"""
"""dest_host->host_name"""
      ]
    }
    {
      EntityType = "device"
      Name = "url"
      Fields = [
"""malware_url->url"""
      ]
    }
      
}
```