#### Parser Content
```Java
{
Name = vmware-carbonblackceedr-sk4-process-create-success-crossproc
  Conditions = [ """endpoint.event.crossproc""", """"process_username":"""", """"event_origin":"EDR"""", """"crossproc_reputation":"""" ]
  ParserVersion = v1.0.0


carbonblack-edr}{
  Name = vmware-carbonblackceedr-sk4-process-create-success-crossproc
  Conditions = [ """endpoint.event.crossproc""", """"process_username":"""", """"event_origin":"EDR"""", """"crossproc_reputation":"""" ]
  ParserVersion = v1.0.0

},

${VMWareParsersTemplates.nsx-config-change-activity} {
 Name = vmware-nsx-str-configuration-modify-success-configcreate
 ParserVersion = "v1.0.0"
 Conditions= [ """Avi-Controller""", """event CONFIG_CREATE""" ]
 },

${VMWareParsersTemplates.nsx-config-change-activity} {
 Name = vmware-nsx-str-configuration-modify-success-configupdate
 ParserVersion = "v1.0.0"
 Conditions= [ """Avi-Controller""", """event CONFIG_UPDATE""" ]
 },

${VMWareParsersTemplates.nsx-config-change-activity} {
 Name = vmware-nsx-str-configuration-modify-success-configdelete
 ParserVersion = "v1.0.0"
 Conditions= [ """Avi-Controller""", """event CONFIG_DELETE""" ]
 },

${VMWareParsersTemplates.airwatch-app-activity}{
  Name = vmware-airwatch-kv-endpoint-login-success-adminuserloggedin
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """AirWatch""", """Event Timestamp:""", """ConsoleEvent: AdminUserLoggedIn""" ]
  Fields = ${VMWareParsersTemplates.airwatch-app-activity.Fields}[
    """Timestamp: ({time}\w+\s\d{1,2}\s\d+:\d+:\d+)"""
    """({result}AdminUserLoggedIn)"""
  
}
```