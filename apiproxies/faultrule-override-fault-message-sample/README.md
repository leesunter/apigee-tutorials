faultrule-override-verifyapikey-message-sample
==============================================
Sample API Proxy to demonstrate how to execute Faultrules and override error message generated by another fault rule.

### Test #1 - Call /resource-that-raises-user-defined-faults

```bash
curl http://testmyapi-test.apigee.net/faultrule-override-fault-message-sample/resource-that-raises-user-defined-faults -v
```

### Test #2 - Call /resource-that-throws-js-exception
```bash
curl http://testmyapi-test.apigee.net/faultrule-override-fault-message-sample/resource-that-throws-js-exception -v
```

### Test #3 Call /resource-that-returns-500-status-code
Note **DefaultFaultRule** executed from Target Endpoint.
```bash
curl http://testmyapi-test.apigee.net/faultrule-override-fault-message-sample/resource-that-returns-500-status-code -v
```

### How to deploy this API Proxy

```bash
apigeetool deployproxy  -u $ae_username -p $ae_password -o testmyapi -e test -n faultrule-override-fault-message-sample -d . -V
```