1. What ConfigMaps and Secrets are and when to use each?

A. A configmap is used to store non sensitive data like environment variables, app settings, feature flags and file paths whereas secret is used to store sensitive data like access tokens, api keys, passwords, etc.

Configmap is used when there is a need to populate environment variables, configuration files in the container volume.
Secrets are used to store database credentials, TLS certificates, authentication tokens, etc.

2. The difference between environment variables and volume mounts

A. Environment variables are key value pairs which are injected into a container when needed whereas volume mounts are specified directory available at specified path of the container, used for data persistence and data sharing.

3. Why base64 is encoding, not encryption?

A. base64 is used for data format translation, not confidentiality nor security. Encoded value can easily be decoded.

4. How ConfigMap updates propagate to volumes but not env vars?

A. It is because the kubelet node periodically syncs changes to mounted files but do not update environment variables which are only set when pod is created.