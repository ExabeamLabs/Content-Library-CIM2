# Code Changes for cimcor-cimtrak-app-activity-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'cimcor-cimtrak-json-app-activity-success-catchall') && InList(toLower(message_id), 's_logmsg_0000000003','s_logmsg_0000000005','s_logmsg_0000000006','s_logmsg_0000000014','s_logmsg_0000000042','s_logmsg_0000000043','s_logmsg_0000000045','s_logmsg_0000000046','s_logmsg_0000000053','s_logmsg_0000000058','s_logmsg_0000000059','s_logmsg_0000000134','s_logmsg_0000000135','s_logmsg_0000000169','s_logmsg_0000000193','s_logmsg_0000000194','s_logmsg_0000000212','s_logmsg_0000000221','s_logmsg_0000000239') |