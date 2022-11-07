#### Parser Content
```Java
{
Name = infoblox-bddi-kv-configuration-modify-success-authzonecreate
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created AuthZone """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Created AuthZone)""",
# auth_zone is removed
# dns_view is removed
# fqdn is removed
# locked is removed
# ms_ad_integrated is removed
# zone_format is removed
# create_ptr_for_bulk_hosts is removed
# create_ptr_for_hosts is removed
# ddns_principal_group is removed
# dns_integrity_check_member is removed
# do_host_abstraction is removed
# use_external_primary is removed
# is_multimaster is removed
# ns_group is removed
# use_import_from is removed
# use_scavenging is removed
  ]
  ParserVersion = "v1.0.0"


}
```