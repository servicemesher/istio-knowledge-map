# **Istio 知识图谱**

## **Istio 介绍**

### **Istio 和服务网格**

- 概念原理

- - Istio

  - - Istio 概述
    - 架构解析

  - 服务网格

  - - 什么是服务网格
    - 服务网格的设计模式

- Istio能带来什么

### **核心功能**

- 流量管理
- 安全
- 可观察性
- 平台支持
- 集成和定制

### **架构**

- Envoy

- - API

  - - MS（Metric 服务）
    - RLS（速率限制服务）

  - xDS 

  - - ADS
    - RDS
    - EDS
    - CDS
    - LDS
    - SDS
    - HDS

  - 扩展 Envoy

- Mixer

- - Policy
  - Telemetry

- Pilot

- Citadel

- Galley

- Egress gateway

- Ingress gateway

- Sidecar injector

- - Mutable webhook

  - Sidecar 注入流程

  - 透明拦截

  - - iptables
    - eBPF

  - Go template

  - Sidecar 的 ConfigMap 配置

  - - istio
    - istio-sidecar-injector

### **设计目标**

### **Istio 与同类产品对比**

- Istio vs Spring Cloud
- Istio vs Linkerd2

## **策略与遥测**

### **Mixer**

- 前置检查
- 配额管理

- 遥测报告

### **适配器**

### **可靠性和延迟**

### **属性**

- 属性词汇
- 属性表达式

### **缓存机制（Mixer Cache）**

### **配置模型**

### **处理器（Handler）**

### **实例（Instance）**

### **规则（Rule）**

**实战**

- 使用Denier 适配器实现白黑名单
- 启用速率限制

## **安全**

### **高级架构**

### **Istio 身份**

- Istio 安全与 SPIFFE

### **PKI**

- Kubernetes 方案
- 本地机器方案
- 代理程序代理节点（开发中）

### **认证**

- 双向 TLS 认证

- - 什么是 TLS？
  - 安全命名

- 认证架构

- 认证策略

- - 策略存储范围
  - 目标选择器
  - 传输认证
  - 来源身份认证
  - 主认证绑定

- 更新认证策略

### **授权和鉴权**

- 授权架构

- 授权许可模式

- 启用授权

- 授权策略

- - ServiceRole
  - ServiceRoleBinding

- 使用其他授权机制

## **多集群部署**

### **多集群服务网格**

- Istio-remote
- 多控制平面拓扑
- 单一控制平面拓扑

## **性能与可伸缩性**

### **微基准测试**

- 什么是基准测试？

### **测试场景**

### **端到端综合基准测试**

### **现实应用程序基准测试**

### **自动化测试**

### **可伸缩性和规模调整指南**

## **日志监控和跟踪**

### **Envoy 和 Mixer**

### **分布式跟踪**

- OpenTracing

- Jaeger
- Zipkin
- Kiali

### **监控**

- Prometheus
- 配置 Metrics 收集
- 获取 TCP 服务指标
- Grafana  可视化图表展示
- 生成服务图

### **日志收集**

- Fluentd
- 配置日志
- 安装 Fluentd/Elasticsearch/Kibana 套件

## **流量管理**

### **Pilot 和 Envoy**

### **请求路由**

- 服务之间的通讯
- Ingress 和 Egress

### **服务发现和负载均衡**

### **故障处理**

- 微调
- FAQ

### **故障注入**

- 延时

- 错误

### **流量转移**

### **熔断**

### **镜像**

### **规则配置**

- 设置请求超时
- A/B 测试
- 灰度发布（金丝雀发布）
- 蓝绿发布

### **Virtual Service**

- 定义
- 规则的目标描述
- HTTP 路由
- TCP 路由
- TLS 路由
- 在服务之间分拆流量
- 超时和重试
- 错误注入
- 跳转和重写
- 跨域资源共享
- 镜像流量
- 添加请求头
- 条件规则
- 多重匹配条件
- 优先级

### **DestinationRule**

- 定义
- 负载均衡
- 连接池
- 健康检查
- 断路器
- TLS
- 规则评估

### **ServiceEntry**

- 定义

### **Gateway**

- 定义
- Gateway vs kubernetes ingress
- Gateway 原理及实现

## **最佳实践**

### **部署**

- Istio Dashboard
- 升级 Istio
- Helm 定制部署 Istio

### **示例**

- 一个请求的完整过程分析

### **升级维护**

- 升级操作步骤
- 升级注意事项
- 无缝升级

### **故障排查**

- 故障排查指南

- 常见故障

- - no healthy upstream 
  - upstream connect error or disconnect/reset before headers
