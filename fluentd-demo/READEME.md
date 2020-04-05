# How to use

```
// using arm base kernel
> docker run --rm --name fluentd -v ${PWD}/fluent.conf:/fluentd/etc/fluent.conf -v ${PWD}/dest_logs:/fluentd/log -v ${PWD}/src_logs:/pod-data fluent/fluentd:v1.10.1-debian-arm64-1.0

// using x86 or x64 kernel
> docker run --rm --name fluentd -v ${PWD}/fluent.conf:/fluentd/etc/fluent.conf -v ${PWD}/dest_logs:/fluentd/log -v ${PWD}/src_logs:/pod-data fluent/fluentd:v1.10-debian-1
```

# Clean up

```
> sudo rm -rf dest_logs && sudo rm src_logs/apache-access.log.pos && sudo rm src_logs/lumne.log.pos && mkdir dest_logs && chmod -R 777 dest_logs
```
