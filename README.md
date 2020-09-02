你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# Canary Release

## About the project

This project implements a canary release system based on [Rudder](https://github.com/caicloud/rudder)

### Status

The project is still in `alpha` version

### Design

Learn more about canary release on [design doc](docs/design.md)

## Getting Started

### Layout

```
├── docs
├── hack
├── build
│   ├── controller
│   ├── nginx-base
│   └── nginx-proxy
│       ├── controller
│       └── etc
├── cmd
│   ├── controller
│   └── nginx-proxy
├── controller
│   ├── bin
│   ├── config
│   └── controller
└── proxies
    └── nginx
├── pkg
│   ├── api
│   ├── chart
│   ├── util
│   └── version
```

Explanation for main pkgs:
- `build` contains dockerfiles for canary release.
- `cmd` contains main packags, each subdirectory of cmd is a main package.
- `docs` for project documentations.
- `controller` contains codes for canary release controller 
- `proxies` contains canary release proxies, each subdirectory is a kind of proxies.
- `pkg` contains utilities for canary release.
