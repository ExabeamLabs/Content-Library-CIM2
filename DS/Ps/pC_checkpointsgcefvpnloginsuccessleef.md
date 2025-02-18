#### Parser Content
```Java
{
Name = "checkpoint-sg-cef-vpn-login-success-leef"
  ParserVersion = v1.0.0
  Conditions = [ """LEEF""", """|Check Point|Connectra|""" ]
} 
]
#=================================================== End of CheckpointParsers section ==================================================================

#================================================== Start of CheckpointParsersDL section =================================================================
CheckpointParsersDL = [
${DLCheckpointParsersTemplates.checkpoint-firewall-2}{
  Name = "checkpoint-ngfw-kv-app-notification-logmsg"
  ParserVersion = "v1.0.0"
  Conditions = [ """CheckPoint""", """log_sys_message:"""" ]
  Fields = ${DLCheckpointParsersTemplates.checkpoint-firewall-2.Fields} [
    """\Wlog_sys_message:"({additional_info}[^"]+)"""
  ]


}
```