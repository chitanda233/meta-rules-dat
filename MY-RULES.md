# 我的自定义规则

这里是本仓库自定义规则的固定入口。日常查看和管理请从默认分支 `master` 打开本文件，不需要手动切换到 `sing` 分支。

## 规则文件

- [强制直连规则 JSON](my-rules/myself-direct.json)
- [强制直连规则 SRS（二进制）](my-rules/myself-direct.srs)
- [代理规则 JSON](my-rules/myself-proxy.json)
- [代理规则 SRS（二进制）](my-rules/myself-proxy.srs)
- [富途规则 JSON](my-rules/futu.json)
- [富途规则 SRS（二进制）](my-rules/futu.srs)

## 维护说明

`my-rules/` 是自定义规则的日常查看和维护入口。为兼容现有 sing-box 规则集路径，`sing` 分支中的 `geo/geosite/myself-direct.*` 和 `geo/geosite/myself-proxy.*` 继续保留。修改这两组规则时，应同步更新这两个位置，确保 JSON 与 SRS 一致。

富途规则合并了上游的 Futu 域名集和 Karing「富途」分组中新增的 `futu.com` 与 IP 网段。[上游规则快照](https://github.com/MetaCubeX/meta-rules-dat/blob/12f5451acf88c4b7e49ec0cca0b20f9cde36bfa7/geo/geosite/futu.json)

修改 `futu.json` 后，在仓库根目录运行 `sing-box rule-set compile --output my-rules/futu.srs my-rules/futu.json` 重新生成 SRS。
