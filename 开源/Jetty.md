# Jetty

Jetty能提供http服务端，http客户端和javax.servlet容器。

## ChangeLog

基于jetty9版本。

### [9.4.42.v20210604](https://github.com/eclipse/jetty.project/releases/tag/jetty-9.4.42.v20210604)

- [#6342](https://github.com/eclipse/jetty.project/pull/6342) - Explain EatWhatYouKill naming

添加注释

- [#6330](https://github.com/eclipse/jetty.project/issues/6330) - CustomRequestLog is missing HTTP version format option
- [#6323](https://github.com/eclipse/jetty.project/issues/6323) - HttpClient gets stuck/never calls onComplete() when multiple requests with timeouts are sent
- [#6308](https://github.com/eclipse/jetty.project/pull/6308) - Ensure buffers are returned to pool by MessageInputStream
- [#6287](https://github.com/eclipse/jetty.project/issues/6287) - Class loading broken for WebSocketClient used inside webapp
- [#6285](https://github.com/eclipse/jetty.project/issues/6285) - HTTP2 client: IllegalStateException: Cannot release an already released entry
- [#6276](https://github.com/eclipse/jetty.project/issues/6276) - Support non-standard domains in SNI and X509
- [#6268](https://github.com/eclipse/jetty.project/issues/6268) - Warnings about "unable to parse form content" are not helpful for troubleshooting
- [#6118](https://github.com/eclipse/jetty.project/issues/6118) - Display a warning when Hazelcast configuration does not contain Jetty session serializer
- [#5931](https://github.com/eclipse/jetty.project/issues/5931) - SslConnection should implement getBytesIn()/getBytesOut()

### [9.4.41.v20210516](https://github.com/eclipse/jetty.project/releases/tag/jetty-9.4.41.v20210516)

- This release resolves [CVE-2021-28169](https://github.com/eclipse/jetty.project/security/advisories/GHSA-gwcr-j4wh-j3cq)

ResourceService & ConcatServlet & WelcomeFilter 传入encode的uri

- [#6099](https://github.com/eclipse/jetty.project/issues/6099) Cipher preference may break SNI if certificates have different key types
- [#6186](https://github.com/eclipse/jetty.project/issues/6186) Add Null Protection on Log / Logger
- [#6205](https://github.com/eclipse/jetty.project/issues/6205) OpenIdAuthenticator may use incorrect redirect
- [#6208](https://github.com/eclipse/jetty.project/issues/6208) HTTP/2 max local stream count exceeded
- [#6227](https://github.com/eclipse/jetty.project/issues/6227) Better resolve race between `AsyncListener.onTimeout` and `AsyncContext.dispatch`
- [#6254](https://github.com/eclipse/jetty.project/issues/6254) Total timeout not enforced for queued requests
- [#6263](https://github.com/eclipse/jetty.project/issues/6263) Review URI encoding in ConcatServlet & WelcomeFilter
- [#6277](https://github.com/eclipse/jetty.project/issues/6277) Better handle exceptions thrown from session destroy listener
- [#6280](https://github.com/eclipse/jetty.project/issues/6280) Copy ServletHolder class/instance properly during startWebapp

### [9.4.40.v20210413](https://github.com/eclipse/jetty.project/releases/tag/jetty-9.4.40.v20210413)

#### Notable Bug Fixes

Users of GzipHandler should upgrade. ([#6168](https://github.com/eclipse/jetty.project/issues/6168))

Users of SSL/TLS on the jetty-server or jetty-client should upgrade. ([#6082](https://github.com/eclipse/jetty.project/issues/6082))

- [#6168](https://github.com/eclipse/jetty.project/issues/6168) - Improve handling of unconsumed content

**[server/HttpInput.java]有接口上的变更**

- [#6148](https://github.com/eclipse/jetty.project/issues/6148) - Jetty start.jar always reports jetty.tag.version as `master`

jar包加载时增加version的help

- [#6105](https://github.com/eclipse/jetty.project/issues/6105) - HttpConnection.getBytesIn() incorrect for requests with chunked content

fillRequestBuffer处理时的bug修复，这个buffer只用来记录log

- [#6082](https://github.com/eclipse/jetty.project/issues/6082) - SslConnection compacting

SslConnection中减少调用BufferUtil.compact的次数，只在BUFFER_UNDERFLOW的状态下调用。

### jetty 9.3到9.4变更