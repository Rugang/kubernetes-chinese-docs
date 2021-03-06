## kubectl create
`译者：hurf` `校对：无`


通过文件名或控制台输入，创建资源。

### 摘要

通过文件名或控制台输入，创建资源。

接受JSON和YAML格式的描述文件。

```
kubectl create -f FILENAME
```

### 示例

```
# 使用pod.json文件创建一个pod
$ kubectl create -f ./pod.json

# 通过控制台输入的JSON创建一个pod
$ cat pod.json | kubectl create -f -
```

### 选项

```
  -f, --filename=[]: 用以创建资源的文件名，目录名或者URL。
  -o, --output="": 输出格式，使用“-o name”来输出简短格式（资源类型/资源名）。
      --schema-cache-dir="/tmp/kubectl.schema": 如果不为空，将API schema缓存为指定文件，默认缓存到“/tmp/kubectl.schema”。
      --validate[=true]: 如果为true，在发送到服务端前先使用schema来验证输入。
```

### 继承自父命令的选项
```
      --alsologtostderr[=false]: 同时输出日志到标准错误控制台和文件。
      --api-version="": 和服务端交互使用的API版本。
      --certificate-authority="": 用以进行认证授权的.cert文件路径。
      --client-certificate="": TLS使用的客户端证书路径。
      --client-key="": TLS使用的客户端密钥路径。
      --cluster="": 指定使用的kubeconfig配置文件中的集群名。
      --context="": 指定使用的kubeconfig配置文件中的环境名。
      --insecure-skip-tls-verify[=false]: 如果为true，将不会检查服务器凭证的有效性，这会导致你的HTTPS链接变得不安全。
      --kubeconfig="": 命令行请求使用的配置文件路径。
      --log-backtrace-at=:0: 当日志长度超过定义的行数时，忽略堆栈信息。
      --log-dir="": 如果不为空，将日志文件写入此目录。
      --log-flush-frequency=5s: 刷新日志的最大时间间隔。
      --logtostderr[=true]: 输出日志到标准错误控制台，不输出到文件。
      --match-server-version[=false]: 要求服务端和客户端版本匹配。
      --namespace="": 如果不为空，命令将使用此namespace。
      --password="": API Server进行简单认证使用的密码。
  -s, --server="": Kubernetes API Server的地址和端口号。
      --stderrthreshold=2: 高于此级别的日志将被输出到错误控制台。
      --token="": 认证到API Server使用的令牌。
      --user="": 指定使用的kubeconfig配置文件中的用户名。
      --username="": API Server进行简单认证使用的用户名。
      --v=0: 指定输出日志的级别。
      --vmodule=: 指定输出日志的模块，格式如下：pattern=N，使用逗号分隔。
```

### 参见

* [kubectl](kubectl.md)	 - 使用kubectl来管理Kubernetes集群。