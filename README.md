# CNCF + Summer of Code

The Cloud Native Computing Foundation participates in Google's Summer of Code (GSoC). CNCF is a great place to spend a summer learning, coding, participating and contributing. We are an exciting open source foundation with a vibrant community of projects, and we look forward to your application and your project ideas!

## Organization Admins

If you need help with anything CNCF + Summer of code related, you can file an issue or contact one of the admins below:

* Chris Aniszczyk (@caniszczyk): https://twitter.com/cra
* Brett Preston (@bpreston)
* Cameron Zahedi (@czahedi)

It's best if you use a public communication channel whenever possible; however, if you need to communicate in private, please feel free to send the admins a note via info@cncf.io (please use the public channels for any project-related discussion).

## Current Year

We are submitting an application as a mentoring organisation for Google Summer of Code 2017.

### Students

You can take a look at our official project ideas list below.

### Mentors

Add your ideas to the README list below.

Also please contact the org admins to add you to the gsoc github team:
https://github.com/orgs/cncf/teams/gsoc-2017-mentors

## Project Ideas

### Kubernetes

#### Improve ThirdPartyResources

* Description: ThirdPartyResources were added some time ago, but the implementation has languished with multiple outstanding capabilities that are missing. They did not complete the list of requirements for graduating to beta (kubernetes/kubernetes#22768).
* Recommended Skills: golang
* Mentor(s): Stefan Schimanski (@sttts)
* Issue: https://github.com/kubernetes/features/issues/95

#### Code metrics infrastructure, measure, report in CI

* Description: The Kubernetes code base grows every day. Reviews mostly concentrate on functionality and architecture, less on code hygiene like test coverage, cyclomatic complexity, linting etc. The goal of this project is to find better ways to support developers and reviewers by making these metrics more visible on new pull-requests. Ideas are to extend our github bots to post a green-yellow-red traffic light for certain measurements or to add new merge gates e.g. if test coverage goes down without being acknowledged by reviewers. 
* Recommended Skills: golang
* Mentor(s): Stefan Schimanski (@sttts)
* Issue:

#### Prototype ssh based replacement for kubctl-exec

* Description: Kubectl exec is implemented with a proprietary protocol. The communication is not end-to-end encrypted. This project is about prototyping the integration of an on-demand SSH server in the kubelet and tunneling of the connection through the apiserver.
* Recommended Skills: golang
* Mentor(s): Stefan Schimanski (@sttts)
* Issue: https://github.com/kubernetes/kubernetes/issues/42950

#### Bazel rules for generated code

* Description: Bazel is Google's internal build tool with more than a decade of history internally, recently OpenSource'ed. It is well suited for big code bases and complex build dependency graphs. Today Kubernetes uses a large GNU make based build system mixed with a lot of bash scripting, which is slow, error prone and more and more unmaintainable. Early work has been done already to compile Kubernetes and to run tests with Bazel. A big next step is to integrate the various code generators that are heavily used in Kubernetes. The goal is better maintainability and much faster turn around cycles for developers and our CI infrastructure.
* Recommended Skills: golang, interest in build systems, able to read existing Makefiles and bash code
* Mentor(s): Stefan Schimanski (@sttts)
* Issue:

#### Create and implement a Data Model to standardize Kubernetes logs

* Description: To perform operations in large kubernetes clusters, where microservices-based applications can be composed of a considerable number of pods, well-structured logs are required. A Data Model that can help find the right field in the right log and tag it (i.e. app name) is required. This way the logs can be easily processed, correlated and queried so the troubleshooting becomes much easier and the time to find root causes for problems gets dramatically reduced. An example implementation can be done with Fluentd ElasticSearch and Kibana
* Recommended Skills: knowledge on Kubernetes internals, basic Ruby coding skills, knowledge on JSON / YAML
* Mentor(s): Peter Portante, Tushar Katarki, Miguel Pérez Colino (backup)
* Issue:

#### Develop a set of Jupyter Notebooks for the Python Client

* Description: The Kubernetes python client  is currently in incubation. Jupyter is the new interactive python interface, it has a web accessible UI and several key features to discovery Python modules as well as interact directly with a shell. In this project, the student will learn the Kubernetes API by using the Python client and develop a set of Notebooks that highlight the Kubernetes primitives. These will all be interactive notebooks that can be run as a Kubernetes applications.
* Recommended Skills: Python
* Mentor(s): Sebastien Goasguen
* Issue: [https://github.com/kubernetes-incubator/client-python/issues/127](https://github.com/kubernetes-incubator/client-python/issues/127)

#### Improve kompose support for docker bundles

* Description: Kompose is a Kubernetes incubator project that translates docker-compose application description into a set of Kubernetes manifests. As docker-compose evolves and new versions are avaialable, kompose needs to keep up. In this project, the student will learn the docker bundle format, evaluate its current use and development state, then improve the kompose bundle support. The student will also participate in the support of docker-compose v3 format.
* Recommended Skills: Golang
* Mentor(s): Sebastien Goasguen
* Issue: [https://github.com/kubernetes-incubator/kompose/issues/390](https://github.com/kubernetes-incubator/kompose/issues/390)

#### Develop advanced Charts for Helm

* Description:  Helm is the package manager for Kubernetes. Application packaged by Helm are called Charts, there are currently over 50 charts in the repository. This project aims at learning Helm and Charts and contributing to Charts development. The student will focus on advanced applications pipelines that use multiple charts as dependencies.
* Recommended Skills: Golang, Kubernetes, Bash
* Mentor(s): Sebastien Goasguen
* Issue: [https://github.com/kubernetes/charts/issues/694](https://github.com/kubernetes/charts/issues/694)

#### TODO

### Fluentd

Fluentd is an open source data collector for unified logging layer: http://www.fluentd.org/

#### Fluentd Monitoring Dashboard
* Description: [Fluentd](http://fluentd.org) as a log collector and aggregator, runs as a service in background, for hence having graphical built-in monitoring capabilities is a must for all scenarios. This project aims to implement a web based dashboard that reports the Fluentd internals from different stages of the data cycle: collection, parsing, filtering, buffering and outputs.
* Recommended Skills: Ruby, API, CSS, Bootstrap and Javascript
* Mentor(s): Eduardo Silva (@edsiper)
* Issue: https://github.com/fluent/fluentd/issues/1475

#### Fluent Bit: plugins development and extend golang interface
* Description: [Fluent Bit](http://fluentbit.io) is a log forwarder that can be integrated with Fluentd or work in standalone mode for log handling. This project aims to extend the number of plugins available to perform data collection, filtering and outputs.
* Recommended Skills: C, TCP, Sockets, Golang and Linux.
* Mentor(s): Eduardo Silva (@edsiper)
* Issue: https://github.com/fluent/fluent-bit/issues/194

### Prometheus

Prometheus is an open-source systems monitoring and alerting toolkit: https://prometheus.io/

#### Add option to log slow queries and recording rules
* Description: Having something like PostgreSQL's log_min_duration_statement would be useful to debug performance problems. It would be great to collect detailed query information, like how many chunks were necessary to compute the result and how many had to be loaded from disk.
* Recommended Skills: golang
* Mentor(s): Ben Kochie (@SuperQ)
* Issue: https://github.com/prometheus/prometheus/issues/1315

#### General purpose rule/alert testing tool
* Description: Write a wrapper that turns (https://github.com/prometheus/prometheus/blob/master/promql/test.go) into a general-purpose rule/alert testing tool.
* Recommended Skills: golang
* Mentor(s): Ben Kochie (@SuperQ)
* Issue: https://github.com/prometheus/prometheus/issues/1695

### linkerd

linkerd is a resilient service mesh for cloud native apps: https://linkerd.io/

#### Adopt OpenTracing in linkerd
* Description: Add opentracing support in linkerd.
* Recommended Skills: Scala
* Mentor(s): Oliver Gould (@olix0r), Andrew Seigner (@siggy)
* Issue: https://github.com/linkerd/linkerd/issues/1079

#### QUIC Netty codec
* Description: Build a QUIC Netty codec.
* Recommended Skills: Java, Netty, UNIX Networking
* Mentor(s): Oliver Gould (@olix0r)
* Issue: https://github.com/linkerd/linkerd/issues/1078

#### Redis protocol support
* Description: Add redis protocol support.
* Recommended Skills: Scala, Finagle, Redis
* Mentor(s): Oliver Gould (@olix0r), Alex Leong (@adleong)
* Issue: https://github.com/linkerd/linkerd/issues/1077

#### MySQL protocol support
* Description: Add mysql protocol support.
* Recommended Skills: Scala, Finagle, MySQL
* Mentor(s): Oliver Gould (@olix0r), Alex Leong (@adleong)
* Issue: https://github.com/linkerd/linkerd/issues/1080

### OpenTracing

[OpenTracing](http://opentracing.io/) is an open standard for distributed tracing. A trace tells the story of a transaction or workflow as it propagates through a (potentially distributed) system. OpenTracing makes it easy for developers to add (or switch) tracing implementations, by offering a vendor-neutral APIs that popular platforms can bind to.

With v1.0 of OpenTracing complete, we are now in the process of intrumenting major web frameworks, services, and networking/controlflow libraries. See [Instrumenting Frameworks](http://opentracing.io/documentation/pages/instrumentation/instrumenting-frameworks.html) for more information.

In addition to the following projects, students may choose an equivalent framework, library, or service, provided it is widely used and Open Source.

#### OpenTracing adaptor for AWS X-Ray 
* Description: X-Ray is a distributed tracing service provided by AWS. X-Ray intrumentation does not currently conform to OpenTracing, it provides a similar (but proprietary) API. Make X-Ray vendor-neutral by building an OpenTracing/X-Ray adaptor, so that it can be plugged in to the OpenTracing ecosystem.
* Recommended Skills: golang
* Mentor(s): Ben Sigelman (@bensigelman)

#### OpenTracing Instrumentation for Nginx, HAProxy, or other Load Balancers
* Description: Load Balancers and Gateways provide a variety of important services, and are present in almost every distributed system. Instrumentation at this layer is often the best first step towards tracing an entire system. Add intrumentation to Nginx, HAProxy, or equilvant gateway service via an OpenTracing plugin. See [Envoy](https://lyft.github.io/envoy/docs/intro/arch_overview/tracing.html) as an example.
* Recommended Skills: C++, nginx 
* Mentor(s): Paul Draper (@pauldraper)

#### Add "net/rpc" and "database/sql" support for Golang
* Description: Instrumented wrappers for the io functionality in Golang's stdlib, such as net/rpc and database/sql, is critical. So far, only net/http has been instrumented. 
* Recommended Skills: golang
* Mentor(s): Paul Draper (@pauldraper)
* Issue: https://github.com/opentracing-contrib/go-stdlib/issues/8

#### go-restful + OpenTracing
* Description: Instrument go-restful (https://github.com/emicklei/go-restful), a wildly used Golang REST web services framework, with OpenTracing.
* Recommended Skills: golang
* Mentor(s): Wu Sheng (@wu-sheng)

### gRPC
[gRPC](grpc.io) is fast and efficient open source RPC framework.

#### gRPC C Core:

* Port gRPC to  one of the major BSD platforms ([FreeBSD](https://freebsd.org), [NetBSD](https://netbsd.org), and [OpenBSD](https://openbsd.org)) and create packages for them. Add [kqueue](https://www.freebsd.org/cgi/man.cgi?query=kqueue) support in the process.
* Required skills: C programming language, BSD operating system.
* Likely Mentors: [Craig Tiller](https://github.com/ctiller),
 [Nicolas Noble](https://github.com/nicolasnoble),
 [Vijay Pai](https://github.com/vjpai).

* Fix gRPC C-core's URI parser. The current parser does not qualify as a standard parser according to [RFC3986]( https://tools.ietf.org/html/rfc3986). Write test suites to verify this and make changes necessary to make the URI parser compliant.
* Required skills: C programming language, HTTP standard compliance.
* Likely mentors: [Craig Tiller](https://github.com/ctiller).

* HPACK compression efficiency evaluation - Figure out how to benchmark gRPC's compression efficiency (both in terms of bytes on the wire and cpu cycles). Implement benchmarks. Potentially extend this to other full-stack gRPC implementations (Java and Go).
* Required skills: C programming language, software performance benchmarking, potentially Java and Go.
* Likely mentors: [Craig Tiller](https://github.com/ctiller).


#### gRPC Python:

* Port gRPC Python to [PyPy](http://pypy.org). Investigate the state of [Cython support](http://docs.cython.org/src/userguide/pypy.html) to do this or potentially explore [cffi](https://cffi.readthedocs.org/en/latest/).
* Required skills: Python programming language, PyPy Python interpreter.
* Likely mentors: [Nathaniel Manista](https://github.com/nathanielmanistaatgoogle), [Masood Malekghassemi](https://github.com/soltanmm).

* Develop and test Python 3.5 Support for gRPC. Make necessary changes to port gRPC and package it for supported platforms.
* Required skills: Python programming language, Python 3.5 interpreter.
* Likely mentors: [Nathaniel Manista](https://github.com/nathanielmanistaatgoogle), [Masood Malekghassemi](https://github.com/soltanmm).
 
#### gRPC Ruby/Java:

* [jRuby](http://jruby.org) support for gRPC. Develop a jRuby wrapper for gRPC based on grpc-java and ensure that it is API compatible with the existing Ruby implementation and passes all tests.
* Required skills: Java programming language, Ruby programming language.
* Likely mentors: [Michael Lumish](https://github.com/murgatroid99), [Eric Anderson](https://github.com/ejona86).


#### gRPC Wire Protocol:

* Develop a [Wireshark](https://wireshark.org) plugin for the gRPC protocol. Provide documentation and tutorials for this plugin.
* Bonus: consider set-up and use with mobile clients.
* Required skills: Wireshark software.
* Likely mentors: [Nicolas Noble](https://github.com/nicolasnoble).

### CoreDNS

CoreDNS is a DNS server that chains middleware.

#### DNSSEC

* Develop/extend the DNSSEC middleware to be able to do on-the-fly-signing and exchanging
  key material with the registrar - in essence implementing zero-touch DNSSEC.
* Required skills: DNSSEC, cryptography, Go
* Mentors: [Miek Gieben](https://github.com/miekg).

#### dnstap Middleware

* Develop a middleware that can use [dnstap](http://dnstap.info/) for DNS data exchange
* Required skills: dnstap, Go
* Mentors: [John Belamaric](https://github.com/johnbelamaric), [Miek Gieben](https://github.com/miekg).

#### etcd3 Support

* Develop a middleware that supports [etcd3 API](https://coreos.com/etcd/docs/latest/v2/api_v3.html) See also https://github.com/coredns/coredns/issues/341
* Required skills: Go
* Mentors: [John Belamaric](https://github.com/johnbelamaric)

### CRI - Container Runtime Interface

[CRI](http://blog.kubernetes.io/2016/12/container-runtime-interface-cri-in-kubernetes.html) is one of the key features of Kubernetes. It is designed to decouple container runtime (e.g. [Docker](https://github.com/docker/docker)) from kubelet by defining a imperative interface for runtimes to follow. Less overhead, less effort and cleaner code base for users to integrate container runtimes into Kubernetes.

#### CRI + Frakti + Unikernels

The goal of this task is to integrate Unikernels as Kubernetes runtime by using Frakti project.

[Frakti](https://github.com/kubernetes/frakti) is an official Kubernetes sub-project which is a well-designed CRI implementation for hypervisor-based runtimes. It now support hypervisor container as well as mixed container runtimes (e.g. Docker + HyperContainer)on same node.

[Unikernels](http://unikernel.org/) are specialised, single-address-space machine images constructed by using library operating systems. You can consider it as a virtual machine but only has a special OS compiled with your applications binaries. Unikernels are considered as the future infrastructure of [IoT](https://en.wikipedia.org/wiki/Internet_of_things) and cloud system.

* Develop a build-in `unikshim` for Frakti to manage Unikernels workloads to serve Kubernetes. Hypervisor manager like libvirt (or QEMU, or even KVM) need to be installed to manage those Unikernels machines and the `unikshim` will be able to communicate with this manager to control the lifecycle of those workloads.
* Required skills: Golang, Operating System knowledge.
* Mentors: [Pengfei Ni](http://github.com/feiskyer), [Harry Zhang](https://github.com/resouer).
* Issue: https://github.com/kubernetes/frakti/issues/99
