#### Parser Content
```Java
{
Name = code42-incydr-str-file-success-logcollector
  ParserVersion = v1.0.0
  Vendor = Code42
  Product = Code42 Incydr
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  time_createdFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  time_modifiedFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions= [ """Code42LogCollector,""", """KAFKA_CONNECT_SYSLOG: """]
  Fields = [ """KAFKA_CONNECT_SYSLOG:\s+({host}[^,]+),(|("+({event_code}[^"]+)"+)|({=event_code}[^,]+)),(|("+({access}[^"]+)"+)|({=access}[^,]+)),(|("+({time}[^"]+)"+)|({=time}[^,]+)),(|("+[^"]+"+)|[^,]+),(|("+({file_path}[^"]+)"+)|({=file_path}[^,]+)),(|("+({file_name}[^"]+)"+)|({=file_name}[^,]+?(\.({file_ext}[^\.,]+))?)),(|("+[^"]+"+)|[^,]+),(|("+({file_type}[^"]+)"+)|({=file_type}[^,]+)),(|("+({bytes}\d+)?"+)|({=bytes}\d+)),(|("+[^"]+"+)|[^,]+),(|("+({hash_md5}[^"]+)"+)|({=md5}[^,]+)),(|("+({hash_sha256}[^"]+)"+)|({=sha256}[^,]+)),(|("+({time_created}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"+)|({=time_created}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)),(|("+({time_modified}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"+)|({=time_modified}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)),(|("+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"+)|({=email_address}[^,]+)),(|("+[^"]+"+)|[^,]+),(|("+({user_uid}[^"]+)"+)|({=user_uid}[^,]+)),(|("+({src_host}[^"]+)"+)|({=src_host}[^,]+)),(|("+[^"]+"+)|[^,]+),(|("+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+)|({=src_ip}[^,]+)),(|("+({additional_info}[^"]+)"+)|({=additional_info}[^,]+)),(|("+({actor}[^"]+)"+)|({=actor}[^,]+)),(|("+({directory_id}[^"]+)"+)|({=directory_id}[^,]+)),(|("+({app}[^"]+)"+)|({=app}[^,]+)),(|("+({url}[^"]+)"+)|({=url}[^,]+)),(|("+({shared}[^"]+)"+)|({=shared}[^,]+)),(|("+({shared_with}[^"]+)"+)|({=shared_with}[^,]+)),(|("+({file_exposure_changed_to}[^"]+)"+)|({=file_exposure_changed_to}[^,]+)),(|("+({cloud_drive_id}[^"]+)"+)|({=cloud_drive_id}[^,]+)),(|("+({detection_source_alias}[^"]+)"+)|({=detection_source_alias}[^,]+)),(|("+({file_id}[^"]+)"+)|({=file_id}[^,]+)),(?:|("+({exposure_type}[^"]+)"+)|({=exposure_type}[^,]+)),(|("+({process_owner}[^"]+)"+)|({=process_owner}[^,]+)),(|("+({process_name}[^"]+)"+)|({=process_name}[^,]+)),(|("+({device_vendor}[^"]+)"+)|({=device_vendor}[^,]+)),(|("+({device_name}[^"]+)"+)|({=device_name}[^,]+)),(|("+({device_id}[^"]+)"+)|({=device_id}[^,]+)),(|("+({device_size}[^"]+)"+)|({=device_size}[^,]+)),(|("+({device_type}[^"]+)"+)|({=device_type}[^,]+)),(|("+({sync_destination}[^"]+)"+)|({=sync_destination}[^,]+))"""
]
  DupFields = ["file_path->file_dir"]


}
```