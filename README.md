# Manus 分流规则

包含 Manus、Cue、Monica 及 Butterfly Effect 旗下相关服务的分流规则。

## Rule Provider

> 以下两种仅为不同的表示方式，作用相同，二选一即可

```yaml
manus: {type: http, format: yaml, behavior: classical, url: "https://raw.githubusercontent.com/yjrszcq/Manus-List/refs/heads/main/manus.yaml", path: ./ruleset/manus.yaml, interval: 86400}
```

```yaml
manus:
  type: http
  format: yaml
  behavior: classical
  url: "https://raw.githubusercontent.com/yjrszcq/Manus-List/refs/heads/main/manus.yaml"
  path: ./ruleset/manus.yaml
  interval: 86400
```

## Rules

> 假设你的 `proxy-groups` 中对 Manus 分流的代理组名为 `MANUS`

```yaml
rules:
  # Manus
  - RULE-SET,manus,MANUS
```
