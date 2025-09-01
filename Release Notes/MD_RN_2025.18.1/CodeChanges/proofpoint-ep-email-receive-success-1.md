# Code Changes for proofpoint-ep-email-receive-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'proofpoint-tappod-cef-email-send-receive-envfrom')InList(type, 'proofpoint-pep-kv-email-receive-envrcpt')InList(type,'proofpoint-tappod-cef-email-send-receive-datarcpt')InList(type,'proofpoint-tappod-cef-email-send-receive-attachment') && (attachment_count != '0' || exists(email_attachment))InList(type,'proofpoint-tappod-cef-email-send-receive-run')InList(type,'proofpoint-tappod-cef-email-send-receive-runfrom')InList(type,'proofpoint-tappod-cef-email-send-receive-msg') && InList(action, 'continue', 'redirect') && ContainsAny(direction, 'default_inbound') |